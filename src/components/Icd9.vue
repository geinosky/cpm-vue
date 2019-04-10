<template>
    <v-container>
        <form class="form-inline mb-3" @submit.prevent="onSubmit">
            <v-text-field label='Enter the phecode' v-model="phecode"></v-text-field>
            <v-btn ml0 color="info" @click="getCodes">Search</v-btn>
        </form>
        <v-data-table
                :headers="headers"
                :items="codes"
        >
            <template v-slot:items="props">
                <td>{{ props.item.code }}</td>
                <td class="text-sx-right">{{ props.item.description }}</td>
            </template>
        </v-data-table>
    </v-container>
</template>

<script>
    import axios from 'axios';

    export default {
        data() {
            return {
                phecode: '',
                codes: [],
                errors: [],
                headers:[
                    {
                        text: 'ICD-9 Code'
                    },
                    {
                        text: 'Description'
                    }
                ]
            }
        },
        methods: {
            async getCodes() {
                axios.get(`http://vumc-env.w83xwsvmxm.us-east-2.elasticbeanstalk.com/icd9?phecode=` + this.phecode)
                    .then(response => {
                        // JSON responses are automatically parsed.
                        this.codes = response.data
                    })
                    .catch(e => {
                        this.errors.push(e)
                    })
            }
        }
    }
</script>