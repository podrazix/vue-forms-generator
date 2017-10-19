<template>
    <div>
        <label>{{ data.label }}</label>
        <input :type="data.type">
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