<template>
  <main class="main-container">
    <header class="header">recommendation</header>
    <div class="div-3"></div>
    <div class="t-shirt">T-Shirt</div>
  </main>
  <form>
    <input type="number" placeholder="temperature in C°" name="temperature" value=""/>
    <button class="button" :openLinkInNewTab="false">refresh</button>
  </form>
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

.input {
  display: flex;
  flex-direction: column;
  position: relative;
  border-radius: 3px;
  border-width: 1px;
  border-style: solid;
  border-color: #ccc;
  width: auto;
  align-self: center;
  height: auto;
  flex-grow: 0;
  max-width: 500px;
  min-height: px;
  font-size: 30px;
  margin: auto;
  padding: 0 10px;
}

.button {
  all: unset;
  display: flex;
  flex-direction: column;
  position: relative;
  appearance: none;
  background-color: black;
  color: white;
  border-radius: 4px;
  text-align: center;
  cursor: pointer;
  width: 100vw;
  max-width: 200px;
  margin: 16px auto 0;
  padding: 10px px 10px 0;
}
</style>
