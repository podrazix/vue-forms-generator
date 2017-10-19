<template>
    <div>
        <label>{{ data.label }}</label>
        <span v-for="value in data.options">
            {{ value }}<input :type="data.type">
        </span>
    </div>
</template>
<script>
    export default{
        props: [
            'data'
        ],
        created(){
            console.log(this.data);
        }
    }
</script>
<style>
</style>