<template>
    <v-card class="py-12 px-4" flat>
        <v-theme-provider dark>
            <div>
                <v-avatar color="primary" size="88">
                    <v-icon large size="64">{{icon}}</v-icon>
                </v-avatar>
            </div>
        </v-theme-provider>
        <v-card-title class="justify-center font-weight-black text-uppercase" v-text="title"></v-card-title>
        <v-card-text class="subtitle-1" v-text="text"></v-card-text>
    </v-card>
</template>
<script lang="ts">
import { defineComponent } from 'vue';
//import { stringifyQuery } from 'vue-router'

export default defineComponent({
    name: 'card1',
    props: {
        icon: String,
        title: String,
        text: String
    },
    setup(props) {
        return {
            icon: props.icon,
            title: props.title,
            text: props.text
        }
    }
})
</script>
