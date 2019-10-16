<template>
  <div class="clock-container">
    <h1>{{ msg }}</h1>
    <h2>Here's my pretty little JS +CSS Clock</h2>

    <div class="clock">
      <div class="clock-face">
        <div class="hand hour-hand"></div>
        <div class="hand min-hand"></div>
        <div class="hand second-hand"></div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Poushita",
  props: {
    msg: String
  },
  created: function() {
    setInterval(this.setDate, 1000);
  },
  methods: {
    setDate: () => {
      const now = new Date();

      const secHand = document.querySelector(".second-hand");
      const seconds = now.getSeconds();
      const secondDegrees = (seconds / 60) * 360;
      secHand.style.transform = `rotate(${secondDegrees}deg)`;

      const minHand = document.querySelector(".min-hand");
      const minutes = now.getMinutes();
      const minuteDegrees = (minutes / 60) * 360 + (seconds / 60) * 6;
      minHand.style.transform = `rotate(${minuteDegrees}deg)`;

      const hourHand = document.querySelector(".hour-hand");
      const hours = now.getHours();
      const hourDegrees = (hours / 12) * 360 + (minutes / 60) * 30;
      hourHand.style.transform = `rotate(${hourDegrees}deg)`;
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.clock-container {
  background: #018ded url(http://unsplash.it/1500/1000?image=881&blur=5);
  background-size: cover;
  font-family: "helvetica neue";
  text-align: center;
  font-size: 10px;
}
.clock {
  width: 20rem;
  height: 20rem;
  border: 20px solid white;
  border-radius: 50%;
  margin: 50px auto;
  position: relative;
  padding: 2rem;
  box-shadow: 0 0 0 4px rgba(0, 0, 0, 0.1), inset 0 0 0 3px #efefef,
    inset 0 0 10px black, 0 0 10px rgba(0, 0, 0, 0.2);
}
.clock-face {
  position: relative;
  width: 100%;
  height: 100%;
  transform: translateY(-3px); /* account for the height of the clock hands */
}
.hand {
  width: 50%;
  height: 6px;
  background: black;
  position: absolute;
  top: 50%;
  transform-origin: 100%;
  transform: rotate(90deg);
  transition: all 0.05s;
  transition-timing-function: cubic-bezier(0.25, 0.1, 0.16, 1.01);
}
</style>
