<template>
    <div class="container">
        <art-form :creator="creator" @submit="submited($event)"></art-form>

        <pre>{{ formData }}</pre>
    </div>
</template>

<script>
    import Form from './components/form.vue';
    export default {
        data(){
            return {
                formData: {},
                creator: [
                    // row 1
                    [
                        {
                            model: 'name',
                            type: 'text',
                            placeholder: 'Wpisz imię',
                            label: 'Imię'
                        },
                        {
                            model: 'surname',
                            type: 'text',
                            placeholder: 'Wpisz nazwisko',
                            label: 'Nazwisko'
                        },
                        {
                            model: 'birth',
                            type: 'date',
                            label: 'Data urodzenia'
                        }
                    ],
                    // row 2
                    [
                        {
                            model: 'email',
                            type: 'text',
                            placeholder: 'Wpisz e-mail',
                            label: 'E-mail'
                        }
                    ]
                ]
            }
        },
        methods: {
            submited(data){
                this.formData = data;
            }
        },
        components: {
            'art-form': Form
        }
    }
</script>

<style>
    pre{
        margin-top: 50px;
    }
</style>
