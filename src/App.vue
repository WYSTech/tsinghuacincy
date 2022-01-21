<template>
  <v-app style="background-color:rgb(241, 199, 245)">
    <!-- <v-navigation-drawer app></v-navigation-drawer> -->
    
    <v-main class="pa-0" >
       <Header />
      <v-container class="pa-0 ma-0" fluid>
        <router-view></router-view>
      </v-container>
    </v-main>
   <v-footer app padless max-height="48" class="bg-purple text-white">
    <v-col
      class="text-center"
      cols="12"
    >
      {{ new Date().getFullYear() }} — <strong>WW</strong>
    </v-col>
  </v-footer>
  </v-app>
</template>

<style lang="scss">

</style>

<script>
import Header from '@/components/Header.vue'
export default {
 components: {
    Header
  }
}
</script>
