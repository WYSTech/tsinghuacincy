<template>
  <v-card>
    <v-img :src="cincy" cover gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.4)" height="40vh">
      <v-app-bar app flat color="transparent" class="text-white">
        <v-app-bar-title></v-app-bar-title>
        <v-spacer></v-spacer>
        <v-btn color="transparent">
          <router-link class="text-white" to="/">Home</router-link>
        </v-btn>
        <v-btn color="transparent">
          <router-link class="text-white" to="/about">About</router-link>
        </v-btn>
      </v-app-bar>
      <v-container style="height: 40vh;">
        <v-row style="height:20vh" align-content="center">
          <img width="64" alt="logo" src="..\assets\Tsinghua_University_Logo.svg" />
          <h1
            style="font-size:4vw; font-family:'KaiTi', cursive; color:rgb(153, 0, 153); -webkit-text-stroke: 0.1px rgb(255, 255, 255);"
          >辛辛那提清华校友会</h1>
        </v-row>
        <!-- <v-row class="ma-16 pa-16"></v-row> -->
        <v-row style="height:20vh" align-content="end">
          <v-card-title class="white--text">
            <p
              style="font-size:3vw; font-family:'Brush Script MT', cursive; color: white; -webkit-text-stroke: 0.5px rgb(153, 0, 153);"
            >Tsinghua Alumni Association of Greater Cincinnati</p>
          </v-card-title>
        </v-row>
      </v-container>
    </v-img>
  </v-card>
</template>

<script lang="ts">
import cincy from '../assets/Cincy.jpg'
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'Header',

  setup() {
    return {
      cincy
    }
  }
})
</script>
