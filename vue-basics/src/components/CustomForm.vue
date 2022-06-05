<template>
  <form @submit.prevent="handleSubmit">
    <h1>{{ title }}</h1>
    <p v-for="(str, idx) in inputs" :key="str">{{ str }} {{ idx }}</p>
    <custom-input v-model="email" :label="emailLabel"/>
    <custom-input v-model="password" :label="passwordLabel"/>
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
            inputs: [
                'email',
                'passwords',
                'name'
            ],
            email: '',
            password: '',
            emailLabel: 'Email',
            passwordLabel: 'Password',
        }
    },
    methods: {
        handleSubmit() {
            console.log(this.email, this.password)
        }
    }
};
</script>

<style>
input, button {
  margin: 10px 0;
  display: block;
}
</style>