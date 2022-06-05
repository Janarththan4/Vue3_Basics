<template>
  <form @submit.prevent="handleSubmit">
    <h1>{{ title }}</h1>
    <custom-input
        v-for="(input,i) in inputs"
        :key="i"
        v-model="input.value" 
        :label="input.label"
        :type="input.type"
    />
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
                {
                label: 'Email',
                value: '',
                type: 'email'
                },
                {
                label: 'Password',
                value: '',
                type: 'password'
                }
            ]
        }
    },
    methods: {
        handleSubmit() {
            console.log(this.inputs[0].value, this.inputs[1].value)
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