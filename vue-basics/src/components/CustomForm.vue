<template>
  <form @submit.prevent="handleSubmit">
    <h1>{{ title }}</h1>
    <input type="text" v-model="email" />
    <input type="password" v-model="password" />
    <button>Log in</button>
  </form>
</template>

<script>
export default {
    data() {
        return {
            title: 'Login Form',
            email: '',
            password: ''
        }
    },
    methods: {
        handleSubmit() {
            // e.preventDefault()
            console.log(this.email, this.password)
        }
    }
};
</script>

<style>
input, button {
  margin: 10px;
  display: block;
}
</style>