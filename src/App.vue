<template>
  <v-app>
    <v-toolbar app>
      <v-toolbar-title class="headline text-uppercase">
        <span>Center for Precision Medicine</span>
      </v-toolbar-title>
    </v-toolbar>

    <v-content>
      <Content />
      <Table />
    </v-content>
  </v-app>
</template>

<script>
import Content from './components/Content'
import Table from './components/Table'

export default {
  name: 'App',
  components: {
    Content,
      Table
  },
  data () {
    return {
      //
    }
  }
}
</script>
