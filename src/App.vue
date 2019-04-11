<template>
  <v-app>
    <v-toolbar app dense class="blue-grey darken-3">
      <v-toolbar-title>
        <a class="white--text" href="https://google.com">Center for Precision Medicine</a>
      </v-toolbar-title>
    </v-toolbar>

    <v-content>
        <v-container>
            <v-layout>

                <v-flex mt-2>
                    <h1 class="display-1 mb-2">
                        Search ICD-9 Codes
                    </h1>
                    <p>
                        Find a phecode's associated ICD-9 codes.
                    </p>
                </v-flex>

            </v-layout>
            <v-flex>
                <Icd9 />
            </v-flex>
        </v-container>
    </v-content>
<v-divider></v-divider>
    <v-footer>
        <v-card
                class="flex"
                flat
                tile
        >
        <v-card-actions class="justify-center">
            Stephen Geinosky - THIS APPLICATION IS A DEMO
        </v-card-actions>
        </v-card>
    </v-footer>
  </v-app>
</template>

<style>
    .v-toolbar__title a {
        text-decoration: none;
    }

    .application {
        font-family: 'Helvetica Neue', Helvetica, Arial, sans-serif;
    }

    .display-1,
    .v-toolbar__title a {
        font-family: 'Nunito', sans-serif !important;
    }
</style>

<script>
    import Icd9 from './components/Icd9'

export default {
  name: 'App',
    components: {
        Icd9
    }
}
</script>
