<template>

<h1>{{ greeting }}</h1>
<input v-model="greeting" />

<hr />

<button v-on:click="isVisible = !isVisible">Toggle Box</button>
<div v-if="isVisible" class="box"></div>
<!-- <div v-else-if="isVisible2" class="box two"></div>
<div v-else class="box three"></div> -->

</template>

<script>
export default {
  data() {
    return {
      greeting: "Hello Vue 3!",
      isVisible: false,
      isVisible2: false,
    }
  }
}

</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@100;200;300;400;500;600;700;800;900&display=swap');
body {
  font-family: 'Poppins', sans-serif;
  background: rgba(0,0,0,.75);
  color: white;
  display: flex;
  align-items: center;
  justify-content: center;
}
.box {
  background: crimson;
  height: 200px;
  width: 200px;
}
.two {
  background: goldenrod;
}
.three {
  background: aqua;
}
[v-cloak] {
  display: none;
}
</style>
