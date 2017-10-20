<template>
    <form>
        <div v-for="(row, key, index) in creator" class="single-row">
            <div v-for="field in row" :style="{'width': (100 / row.length) + '%'}" >
                <component :is="'art-' + field.type" :data="field" v-model="formData[field.model]"></component>
            </div>
            <hr/>
        </div>
        <button class="btn btn-primary" @click.prevent="submit()">Submit!</button>
    </form>
</template>

<script>
    import Check from './fields/check.vue';
    import Date from './fields/date.vue';
    import Radio from './fields/radio.vue';
    import Text from './fields/text.vue';
    export default {
        props: [
            'creator'
        ],
        data() {
            return {
                formData: {}
            }
        },
        methods: {
            submit(){
                this.$emit('submit', this.formData);
            }
        },
        components: {
            'art-check-box': Check,
            'art-date': Date,
            'art-radio': Radio,
            'art-text': Text
        }
    }
</script>

<style>
    .single-row {
        display: flex;
        align-items: center;
        margin: 0 -10px;
    }

    .filed {
        display: flex;
        flex-direction: column;
        padding: 0 10px;

    }

    .filed input{
        height: 50px;
    }
</style>