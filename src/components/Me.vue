<template>
  <div>
    <v-button></v-button>
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from "vue-property-decorator";

@Component
export default class Me extends Vue {
  @Prop() private msg!: string;
}
</script>

<style scoped lang="scss"></style>
