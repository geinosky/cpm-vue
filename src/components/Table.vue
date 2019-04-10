<template>
    <div class="row col-12">
        <Form />
        <Results />
    </div>
</template>

<script>
    import Form from './Form'
    import Results from './Results'

    export default {
        name: 'App',
        components: {
            Form,
            Results
        },
        data () {
            return {
                //
            }
        }
    }
</script>