<template>
  <div id="app">
    <h1>Roll the dice!</h1>
    <Dice />
  </div>
</template>

<script>
import Dice from './components/Dice.vue'

export default {
  name: 'App',
  components: {
    Dice
  }
}
</script>

<style>
#app {
  background-color: #41b883 !important;
  font-family:'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
  position: fixed;
  top: 0;
  left: 0;
  height: 100%;
  width: 100%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
h1 {
  color: #ffffff;
  font-weight: bold;
  font-size: 2.6em;
  margin: 0;
  padding: 0;
  text-shadow: 2px 2px 0px #000000,
              2px 2px 5px #2b7a57;
}
</style>
