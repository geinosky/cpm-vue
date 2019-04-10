<template>
    <v-container>
        <form class="form-inline mb-3" @submit.prevent="onSubmit">
            <div class="form-group mr-3">
                <input class="form-control" name="phecode" id="phecode" aria-label="Enter a phecode" placeholder="Enter a phecode" v-model="phecode">
            </div>
            <button class="btn btn-primary" v-on:click="getCodes">Search</button>
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