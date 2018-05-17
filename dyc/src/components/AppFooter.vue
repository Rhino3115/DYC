<template>
  <v-footer fixed height="auto" class='elevation-15'>
    <v-layout row wrap justify-center>
      <v-btn
        v-for="link in links"
        :key="link"
        flat
      >
        {{ link }}
      </v-btn>
      <v-flex xs12 py-3 text-xs-center>
        &copy;2018 — <strong>DYC</strong>
      </v-flex>
    </v-layout>
  </v-footer>
</template>


<script>
  export default {
    data: () => ({
      links: ['OneDiver', 'Google Drive', 'Xero']
    })
  }
</script>