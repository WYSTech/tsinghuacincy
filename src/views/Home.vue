<template>
  <div class="home">
    <v-container class="text-center">
      <v-row>
        <v-col cols="12" md="6">
          <card :icon="icon" :title="title" :text="text" />
        </v-col>
        <v-col cols="12" md="6">
          <card :icon="icon" :title="title" :text="text" />
        </v-col>
      </v-row>

      <v-row>
        <v-col v-for="({ src, text, title }, i) in articles" :key="i" cols="12" md="4">
          <event :imageSrc="src" :title="title" :text="text"></event>
        </v-col>
      </v-row>
    </v-container>
    <!-- <img alt="Vue logo" src="../assets/logo.png"> -->
    <!-- <HelloWorld msg="Welcome to Your Vue.js + TypeScript App"/> -->
  </div>
</template>

<script lang="ts" setup>
import { onMounted, ref } from 'vue';
import card from '../components/Card1.vue'
import event from '../components/Event.vue'
let icon = 'mdi-shield-outline';
let title = 'Long-term Support';
let text = 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Iusto cupiditate sint possimus quidem atque harum excepturi nemo velit tempora! Enim inventore fuga, qui ipsum eveniet facilis obcaecati corrupti asperiores nam'
let articles = ref({});
onMounted(() => {
  fetch("articles.json")
    .then(response => response.json()
      .then(data => {
        articles.value = data.items;
      }));
});
</script>
