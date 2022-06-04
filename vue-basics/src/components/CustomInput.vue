<template>
    <label>
        {{ label }}
        <input type="text"/>
    </label>
</template>

<script>
export default {
    name: "CustomInput",
    
    data() {
        return {
            
        }
    },

    props: ['label']
}
</script>

<style>

</style>