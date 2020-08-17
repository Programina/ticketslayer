<template>
  <v-app>
    

    <v-main>
      <!-- <HelloWorld /> -->
      <Me />
    </v-main>
  </v-app>
</template>

<script lang="ts">
import Vue from "vue";
import Me from "./components/Me.vue";

export default Vue.extend({
  name: "App",

  components: {
    Me  
  },

  data: () => ({
    //
  })
});
</script>

<style lang="scss">

  .body {
    font-family:'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
    color: 
  }
</style>