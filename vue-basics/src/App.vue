<template>

<custom-form />

</template>

<script>
import CustomForm from './components/CustomForm.vue'

export default {
  components: {
    CustomForm,
  },
  data() {
    return {
      greeting: "Hello Vue 3!",
      isVisible: false,
      // isVisible2: false,
    }
  },
  methods: {
    toggleBox() {
      this.isVisible = !this.isVisible;
    },
    greet(greeting) {
      console.log(greeting)
    }
  }
};

</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@100;200;300;400;500;600;700;800;900&display=swap');

body {
  margin: 0; padding: 0;
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
