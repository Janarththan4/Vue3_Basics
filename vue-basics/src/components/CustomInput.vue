<template>
    <label>
        {{ label }}
        <input :type="type" v-model="inputValue"/>
    </label>
</template>

<script>
export default {
    name: "CustomInput",
    
    // data() {
    //     return {
    //         inputValue: ''
    //     }
    // },

    props: ['label', 'type', 'modelValue'],

    computed: {
        inputValue: {
            get() {
                return this.modelValue
            },
            set(value) {
                // console.log(value)
                this.$emit('update:modelValue', value)
            }
        }
    } 
}
</script>

<style>

</style>