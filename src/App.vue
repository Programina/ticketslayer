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

  *, ::before, ::after {
    box-sizing: border-box;
  }

  .body {
    font-family:'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
    color: #292528;
    padding: 30px;
  }

  .primary {
    color: #F9A03D;
  }

  .primary-bg {
    background-color: #F9A03D;
  }

   .primary-light {
    color: #FAB94C;
  }

  .primary-light-bg {
    background-color: #FAB94C;
  }

  .secondary-cl {
    color: #3EC5FB;
  }

  .secondary-cl-bg {
    background-color: #3EC5FB;
  }

   .secondary-light {
    color: #ADE6FF;
  }

  .secondary-light-bg {
    background-color: #ADE6FF;
  }

  .alert {
    color: #D64550;
  }

  .alert-bg {
    background-color: #D64550;
  }

  .success {
    color: #44AF69;
  }

  .success-bg {
    background-color: #44AF69;
  }

  .brown {
    color: #90583C;
  }

  .brown-bg {
    background-color: #90583C;
  }

  .white-cl {
    color: white;
  }



</style>