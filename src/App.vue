<template>
  <v-app>
    <v-toolbar app>
      <v-toolbar-title class="headline text-uppercase">
        <a href="https://google.com">Center for Precision Medicine</a>
      </v-toolbar-title>
    </v-toolbar>

    <v-content>
        <v-container>
            <v-layout>

                <v-flex mt-4 mb-4>
                    <h1 class="display-2 font-weight-bold mb-3">
                        Search ICD-9 Codes
                    </h1>
                    <p class="subheading font-weight-regular">
                        Find a phecode's associated ICD-9 codes.
                    </p>
                </v-flex>

            </v-layout>
            <v-flex>
                <Icd9 />
            </v-flex>
        </v-container>
    </v-content>

  </v-app>
</template>

<script>
    import Icd9 from './components/Icd9'

export default {
  name: 'App',
    components: {
        Icd9
    }
}
</script>
