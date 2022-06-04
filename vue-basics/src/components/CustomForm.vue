<template>
  <form @submit.prevent="handleSubmit">
    <h1>{{ title }}</h1>
    <custom-input type="text" v-bind:label="emailLabel"/>
    <custom-input type="password" v-bind:label="passwordLabel"/>
    <button>Log in</button>
  </form>
</template>

<script>
import CustomInput from './CustomInput.vue'

export default {
    name: "CustomForm",

    components: {
        CustomInput,
    },
    data() {
        return {
            title: 'Login Form',
            email: '',
            password: '',
            emailLabel: 'Email',
            passwordLabel: 'Password',
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