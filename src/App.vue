<template>
<div class="root">
<properties :img="images"/>

</div>
 
</template>

<script>
import Properties from './components/Properties.vue';
export default {
  components: { Properties },
  name: "App",
  data() {
    return {
      images: [
        "./src/assets/flo.jfif",
        "./src/assets/download.jfif",
        "./src/assets/4.jfif",
        "./src/assets/flo5.jfif",
        "./src/assets/5.jfif"
        
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

