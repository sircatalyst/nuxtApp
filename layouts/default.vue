<template>
  <div>
    <v-toolbar>
      <v-toolbar-title>Learning Nuxt</v-toolbar-title>

      <v-spacer></v-spacer>

      <v-toolbar-items>
        <v-btn text>
          <n-link to="/">Home</n-link>
        </v-btn>
        <v-btn text>
          <n-link to="/about">About</n-link>
        </v-btn>
        <v-btn text>
          <n-link to="/inspire">Inspire</n-link>
        </v-btn>
        <v-btn text>
          <n-link to="/weather-app">Weather App</n-link>
        </v-btn>
      </v-toolbar-items>

      <template v-if="$vuetify.breakpoint.smAndUp">
        <v-btn icon>
          <v-icon>mdi-export-variant</v-icon>
        </v-btn>
        <v-btn icon>
          <v-icon>mdi-delete-circle</v-icon>
        </v-btn>
        <v-btn icon>
          <v-icon>mdi-plus-circle</v-icon>
        </v-btn>
      </template>
    </v-toolbar>
    <nuxt />
  </div>
</template>

<script>
export default {}
</script>
