<template>

<h1>{{ greeting }}</h1>
<input v-model="greeting" />
<hr />

<div v-if="isVisible" class="box"></div>
<div v-else-if="isVisible2" class="box two"></div>
<div v-else class="box three"></div>


</template>

<script>
export default {
  data() {
    return {
      greeting: "Hello Vue 3!",
      isVisible: false,
      isVisible2: true, 
    }
  }
}

</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@100;200;300;400;500;600;700;800;900&display=swap');
body {
  font-family: 'Poppins', sans-serif;
  background: rgba(0,0,0,.75);
  text-align: center;
  color: white;
}
.box {
  background: indigo;
  height: 200px;
  width: 200px;
}
.two {
  background: crimson;
}
.three {
  background: darkgreen;
}
</style>
