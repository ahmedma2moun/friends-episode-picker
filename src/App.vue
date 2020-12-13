<template>
  <div id="app">
    <img src="./assets/aa616123f3055dec749263abe76cf8c3.jpg" />
    <div class="main">
      <button @click="test()">Pick EPS</button>
      <div id="episodes"></div>
    </div>
  </div>
</template>

<script>
export default {
  name: "App",
  methods: {
    test() {
      var eps = [24, 24, 25, 24, 24, 25, 24, 24, 24, 18];
      var season = parseInt(Math.random() * eps.length - 1);
      var episode = parseInt(Math.random() * eps[season] - 1);
      document.getElementById("episodes").textContent = `S${season + 1} E${
        episode + 1
      }`;
    },
  },
};
</script>

<style>
button {
  background-color: white;
  color: red;
  border: 2px solid red;
  border-radius: 10%;
  /* Green */
}

img {
  width: 100%;
  margin-bottom: 2px;
}

.main {
  text-align: center;
}
</style>
