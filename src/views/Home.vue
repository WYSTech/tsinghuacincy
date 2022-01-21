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

<script lang="ts">
import { defineComponent } from 'vue';
import card from '../components/Card1.vue'
import event from '../components/Event.vue'

export default defineComponent({
  name: 'Home',
  components: {
    card, event
  },
  setup() {
    let icon = 'mdi-shield-outline';
    let title = 'Long-term Support';
    let text = 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Iusto cupiditate sint possimus quidem atque harum excepturi nemo velit tempora! Enim inventore fuga, qui ipsum eveniet facilis obcaecati corrupti asperiores nam'

    let articles = [
      {
        src: '/src/assets/Cincy.jpg',
        title: 'Mobile first & Responsive',
        text: 'Phasellus lorem enim, luctus ut velit eget, convallis egestas eros. Sed ornare ligula eget tortor tempor, quis porta tellus dictum.',
      },
      {
        src: '/src/assets/Cincy.jpg',
        title: 'Think outside the box',
        text: 'Nam ut leo ipsum. Maecenas pretium aliquam feugiat. Aenean vel tempor est, vitae tincidunt risus. Sed sodales vestibulum nibh.',
      },
      {
        src: '/src/assets/Cincy.jpg',
        title: 'Small changes, big difference',
        text: 'Vestibulum in dictum velit, in rhoncus nibh. Maecenas neque libero, interdum a dignissim in, aliquet vitae lectus. Phasellus lorem enim, luctus ut velit eget.',
      },
    ];
    return {
      icon,
      title,
      text,
      articles
    }
  }
});
</script>
