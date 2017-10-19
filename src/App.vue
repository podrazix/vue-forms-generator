<template>
    <div class="container">
        <art-form :creator="creator"></art-form>
    </div>
</template>

<script>
    import Form from './components/form.vue';
    export default {
        data(){
            return {
                creator: [
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
                    [

                        {
                            model: 'gender',
                            type: 'radio',
                            options: ['Male', 'Female'],
                            label: 'Płeć'
                        },
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
        components: {
            'art-form': Form
        }
    }
</script>

<style></style>
