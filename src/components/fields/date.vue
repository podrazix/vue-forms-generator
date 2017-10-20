<template>
    <div class="form-group filed">
        <label>{{ data.label }}</label>
        <input class="form-control" type="date" v-model.lazy="some" :placeholder="data.placeholder">
    </div>
</template>
<script>
    export default{
        props: [
            'data',
            'value'
        ],
        data(){
            return {
                some: ''
            }
        },
        watch: {
            some(){
                this.$emit('input', this.some);
            }
        }
    }
</script>
<style>
</style>