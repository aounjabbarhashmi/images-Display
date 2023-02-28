<template>
  <div class="container">
    <div v-for="item in card">
      <img v-bind:src="item" />
    </div>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      card: [
        "./src/assets/flo.jfif",
        "./src/assets/download.jfif",
        "./src/assets/4.jfif",
        "./src/assets/flo5.jfif",
        
      ],
    };
  },
};
</script>

<style>
html {
  overflow-x: hidden;
}
.container {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  align-items: center;
  gap: 1rem;
  width: 100vw;
  height: 100vh;
}
img {
  width: 300px;
  border-radius: 7px;
}
</style>

