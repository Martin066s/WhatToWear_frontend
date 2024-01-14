<template>
  <div class="about">
    <div class="container min-vh-50 d-flex justify-content-center align-items-center">
    <table class="table table-sm" id="clothing-table">
      <thead>
      <tr>
        <th scope="col">Name</th>
        <th scope="col">minTemp</th>
        <th scope="col"></th>
      </tr>
      </thead>
      <tbody id="clothes-table">
      </tbody>
    </table>
  </div>
  </div>
</template>

<style>
#deleteButton {
  background-color: #e61919;
  border-color: #e61919;
}
</style>

<script setup>
import { onMounted } from 'vue'

onMounted(() => {
  draw()
})

function draw () {
  const requestOptions = {
    method: 'GET',
    redirect: 'follow',
    Accept: 'application/json'
  }

  console.log(fetch('http://localhost:8090/Clothing', requestOptions)
    .then(function (response) {
      return response.json()
    }).then(function (obj) {
      const tbodyRef = document.getElementById('clothes-table')
      // console.log(obj[0].name)
      for (let i = 0; i < obj.length; i++) {
        // var tbodyRef = document.getElementById('clothes-table').insertRow);
        console.log(obj[i].name)
        console.log(obj[i].minTemp)
        tbodyRef.innerHTML += `
        <tr id="${obj[i].id}">
        <th scope="row">${obj[i].name}</th>
        <td>${obj[i].minTemp}</td>
        <td><button type="button" id="deleteButton" class="btn btn-primary btn-sm">delete</button></td>
        </tr>
        `
      }
    })
    .catch(error => console.log('error', error)))
}

</script>
