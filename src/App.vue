<template>
  <div class="container">
    <div class="qoute">
      <h1>The earth laugh in flowers</h1>
    </div>
    <div v-for="item in card" :key="item.id">
      <img :src="item.img" />
    </div>
  </div>
</template>

<script>
import axios from "axios";
export default {
  data() {
    return {
      card: [],
    };
  },
  methods: {
    async loadData() {
      let result = await axios.get("http://localhost:3000/card");
      this.card = result.data;
    },
  },
  mounted() {
    this.loadData();
  },
};
</script>

<style>
body {
  overflow-x: hidden;
  box-sizing: border-box;
}
.qoute {
  color: #b06ab3;
  text-align: center;

  font-size: 40px;
  font-family: "Lucida Sans", "Lucida Sans Regular", "Lucida Grande",
    "Lucida Sans Unicode", Geneva, Verdana, sans-serif;
}
.container {
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  justify-content: center;
  align-items: center;
  gap: 1rem;
}
img {
  width: 250px;
  height: 400px;
  border-radius: 7px;
}
</style>

