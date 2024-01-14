<template>
  <main class="main-container">
    <header class="header">recommendation</header>
    <div class="div-3"></div>
    <div class="t-shirt">T-Shirt</div>
  </main>
  <div class="container min-vh-50 d-flex justify-content-center align-items-center">
    <div class="form-group">
      <input type="number" class="form-control" placeholder="current temperature" v-model="minTemp">
    </div>
  </div>
  <button type="button" v-on:click="addClothing()" class="btn btn-primary" id="saveButton">refresh</button>
</template>

<style scoped>
.main-container {
  justify-content: center;
  align-items: center;
  display: flex;
  max-width: 291px;
  flex-direction: column;
  margin: 0 auto 15px;
}

.header {
  color: #000;
  align-self: start;
  width: 100%;
  font: 500 28px Della Respira, sans-serif;
}

.div-3 {
  background-color: #d9d9d9;
  align-self: center;
  display: flex;
  min-height: 332px;
  width: 100%;
  flex-direction: column;
  margin: 6px 25px 0 2px;
}

.t-shirt {
  color: #000;
  text-align: center;
  margin: 21px 0 -3px;
  font: 500 28px Della Respira, sans-serif;
}
</style>

<script>

</script>
