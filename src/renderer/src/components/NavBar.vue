<template>
  <v-toolbar>
    <v-app-bar-nav-icon></v-app-bar-nav-icon>

    <v-toolbar-title>Title</v-toolbar-title>

    <v-spacer></v-spacer>

    <v-select
      v-model="konten"
      :items="kontenfilter"
      label="Konten"
      multiple
      chips
      persistent-hint
      style="min-width: 100px"
    ></v-select>

    <v-select
      v-model="einausgabe"
      :items="einausgabefilter"
      label="'Einnahme/Ausgabe'"
      multiple
      chips
      persistent-hint
      style="min-width: 100px"
    ></v-select>

    <v-select
      v-model="labels"
      :items="labelsfilter"
      label="Labels"
      multiple
      chips
      persistent-hint
      style="min-width: 100px"
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
      konten: [],
      kontenfilter: ['Konto1', 'Bargeld', 'Konto2'],
      einausgabe: [],
      einausgabefilter: ['Einnahme', 'Ausgabe'],
      labels: [],
      labelsfilter: ['Label1', 'Label2', 'Label3']
    }
  }
})
</script>
