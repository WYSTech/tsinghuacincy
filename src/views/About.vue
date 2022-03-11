<template>
  <v-card class="pa-12 ma-12" max-width="1200">
    <v-sheet
      style="top:-32px; position:relative; background-color: #4caf50"
      class="mx-auto"
      elevation="12"
      max-width="calc(100% - 12px)"
    >
      <v-list-item>
        <v-list-item-avatar tile>
          <v-icon color="white" large>mdi-information</v-icon>
        </v-list-item-avatar>
        <v-list-item-content>
          <v-list-item-title class="title" style="color: white">About Us</v-list-item-title>
          <v-list-item-subtitle>{{ new Date().toLocaleDateString() }}</v-list-item-subtitle>
        </v-list-item-content>
      </v-list-item>
    </v-sheet>

    <v-card-text>{{text}}</v-card-text>

    <v-card-actions>
      <v-btn color="green">Contact Us</v-btn>
    </v-card-actions>
  </v-card>
</template>
<script lang="ts">

//import about from "/public/about.json";
import { defineComponent } from 'vue';

export default defineComponent({
    data() {
      return {
        text: ""
      }
    },
    setup() {
    
  },
  mounted() {
    fetch("about.json")
    .then (response=> response.json()
    .then(data=>this.text=data.text));
  }
})

</script>