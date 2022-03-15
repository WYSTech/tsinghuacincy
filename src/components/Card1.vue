<template>
    <v-card class="py-12 px-4" flat>
        <v-theme-provider dark>
            <div>
                <v-avatar color="primary" size="88">
                    <v-icon large size="64">{{ icon }}</v-icon>
                </v-avatar>
            </div>
        </v-theme-provider>
        <v-card-title class="justify-center font-weight-black text-uppercase" v-text="title"></v-card-title>
        <v-card-text class="subtitle-1" v-text="text"></v-card-text>
    </v-card>
</template>
<script lang="ts" setup>
defineProps({
    icon: String,
    title: String,
    text: String
});
</script>
