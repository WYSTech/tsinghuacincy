<template>
    <v-img :src="src" class="mb-4" height="275" max-width="100%"></v-img>
    <h3 class="font-weight-black mb-4 text-uppercase" v-text="title"></h3>
    <div class="title font-weight-light mb-5" v-text="text"></div>
    <v-btn class="ml-n4 font-weight-black" text>Continue Reading</v-btn>
</template>
<script>
import { defineComponent } from "vue";

export default defineComponent({
    name: 'event',
    props: {
        imageSrc: String,
        title: String,
        text: String
    },

    setup(props) {
        return {
            src: props.imageSrc,
            title: props.title,
            text: props.text
        }
    }
})
</script>