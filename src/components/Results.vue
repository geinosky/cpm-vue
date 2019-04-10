<template>
    <v-data-table
            :headers="headers"
            :icd9="icd9"
    >
        <template v-slot:icd9="props">
            <td>{{ props.item.code }}</td>
            <td class="text-sx-right">{{ props.item.description }}</td>
        </template>
    </v-data-table>
</template>

<script>
    export default {
        data() {
            return {
                headers: [
                    {
                        text: 'ICD-9 code',
                        value: 'code',
                    },
                    {
                        text: 'Description',
                        value: 'description'
                    }
                ],
                icd9: []
            }
        }
    }
</script>