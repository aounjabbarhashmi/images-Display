<template>
     <div class="container">
    <div v-for="item in img" :key="item" >
      <img v-bind:src="item" />
    </div>
  </div>
</template>
<script>
export default {
    name:'properties',
    props:{
        img:Array
    }
}
</script>