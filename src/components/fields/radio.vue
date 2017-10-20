<template>
    <div>
        <label>{{data.label}}</label>
        <div class="radio-field">
            <div class="form-check form-check-inline" v-for="value in data.options">
                <label class="form-check-label">
                    <input class="form-check-input" type="radio" :name="'radio'+value" :id="'radio'+value"
                           :value="value"> {{ value }}
                </label>
            </div>
        </div>
    </div>
</template>
<script>
    export default{
        props: [
            'data'
        ]
    }
</script>
<style>
    .radio-field {
        display: flex;
        flex-direction: row;
        align-items: center;
    }
</style>