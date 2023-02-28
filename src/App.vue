<template>

  <h1 class="qoute">The earth laugh in flowers</h1>
  <div class="container">
    <div v-for="item in card" :key="item">
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
        "./public/flo.jfif",
        "./public/download.jfif",
        "./public/4.jfif",
        "./public/flo5.jfif",
        "./public/5.jfif"
        
      ],
    };
  },
};
</script>

<style>
body {
  overflow-x: hidden;
  box-sizing: border-box;
}
.qoute{
  color:  #b06ab3;
  margin-top: 90px;
  text-align: center;

  font-size: 40px;
  font-family: 'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
}
.container {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  align-items: center;
  gap: 1rem;
 padding-top: 20px;
}
img {
  width: 250px;
  height: 400px;
  border-radius: 7px;
}
</style>

