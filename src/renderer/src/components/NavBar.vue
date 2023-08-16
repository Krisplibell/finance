<template>
  <v-toolbar>
    <v-app-bar-nav-icon></v-app-bar-nav-icon>

    <v-toolbar-title>Title</v-toolbar-title>

    <v-spacer></v-spacer>

    <v-select
      v-model="favorites"
      :items="filter"
      label="'Filter'"
      multiple
      hint="Pick your favorite states"
      persistent-hint
    ></v-select>

    <v-btn icon>
      <v-icon>mdi-heart</v-icon>
    </v-btn>

    <v-btn icon>
      <v-icon>mdi-dots-vertical</v-icon>
    </v-btn>
  </v-toolbar>
</template>

<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
  data() {
    return {
      favorites: [],
      filter: ['Ausgaben', 'Eingaben', 'Konto1', 'Label1', 'Label2']
    }
  }
})
</script>
