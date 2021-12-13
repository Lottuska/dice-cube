<template>
  <div class="container">
    <div class="cube">
      <img v-if="number !== null" :src="numberImage" :alt="'Dice value is currently ' + number" draggable="false" />
    </div>
    <button class="button" v-on:click="randomNumber">Roll</button>
  </div>
</template>

<script>
export default {
  name: "Dice",
  data() {
    return {
      number: null,
      numberImage: null,
    };
  },
  methods: {
    randomNumber: function () {
      this.number = Math.floor(Math.random() * 6 + 1); // Random number between 1 to 6
      switch (this.number) {
        case 1:
          this.numberImage = "images/1.png";
          break;
        case 2:
          this.numberImage = "images/2.png";
          break;
        case 3:
          this.numberImage = "images/3.png";
          break;
        case 4:
          this.numberImage = "images/4.png";
          break;
        case 5:
          this.numberImage = "images/5.png";
          break;
        case 6:
          this.numberImage = "images/6.png";
          break;
        default:
          this.numberImage = "";
      }
    },
  },
};
</script>

<style>
.container {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
.cube {
  margin: 100px 0px;
  height: 80px;
  width: 80px;
  border-radius: 8px;
  background-color: #ffffff;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  box-shadow: 2px 7px 7px #2b7a57;
}
.cube img {
  width: 70px;
}
.button {
  padding: 20px;
  width: 220px;
  background-color: #ffffff;
  border: none;
  color: #41b883;
  box-shadow: 2px 7px 7px #2b7a57;
  font-weight: bold;
}
.button:hover {
  box-shadow: 2px 4px 4px #2b7a57;
  cursor: pointer;
}
</style>