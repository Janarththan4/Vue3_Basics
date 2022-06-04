<template>

<h1>{{ greeting }}</h1>
<input v-model="greeting" />


</template>

<script>
export default {
  data() {
    return {
      greeting: "Hello Vue 3!"
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
</style>
