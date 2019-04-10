<template>
    <v-form
        v-model="valid"
        lazy-validation
    >
        <v-text-field
                v-model="phecode"
                label="Enter a phecode"
                required
        ></v-text-field>
        <v-btn
                flat
                href="https://github.com/vuetifyjs/vuetify/releases/latest"
                target="_blank"
        >
            <span class="mr-2">Search</span>
        </v-btn>
    </v-form>
</template>