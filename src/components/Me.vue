<template>
  <div>
    <div class="grid-container">
      <div class="profile-data">
        <h2>Profile</h2>
        <span class="inline-group"><h4>Name: </h4> <div>{{name}}</div> </span>
        Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged.

         <v-btn color="green" @click="remindOfSuccess()">Success!</v-btn>
      </div>
      <div class="quest-data">quest data, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged..</div>
      <div class="side-quest-data">Side quest data,  It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum</div>  
      <div class="item4"><img src="./../assets/warriorprincess.jpg" height="100%" width="330px"></div>
      <div class="item5">5</div>
      <div class="item6">6</div>
      <div class="item7">7</div>
    </div>
   
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from "vue-property-decorator";

@Component
export default class Me extends Vue {
  // @Prop() private msg!: string;
  levelCount: number = 1;
  name: string = 'Amina';

  remindOfSuccess() {
    this.levelCount = this.levelCount++;
    console.log("Level count", this.levelCount)
    alert("Wow, you went up 1 level! That's now at Level " + this.levelCount + "!")
  }
}
</script>

<style scoped lang="scss">

  .grid-container {
    display: grid;
    grid-gap: 10px;
    grid-template-columns: 1fr 2fr;
    grid-template-rows: 2fr 0.5fr 0.5fr 1fr 2fr;
  }

  .profile-data {
    grid-area: 1 / 1 / span 1 / span 1;
    background-color: lightcoral;
  }
 
  .quest-data {
    grid-area: 2 / 1 / span 1 / span 1;
    background-color: purple;
  }

  .side-quest-data {
    grid-area: 3 / 1 / span 1 / span 1;
    background-color: greenyellow;
  }

  .inline-group {
    display: flex;
    flex-direction: row;
    justify-content: flex-start;
    
    div {
      margin-left: 10px;
    }
  }
  
  /**
  .item1 {
    grid-area: 2 / 1 / span 2 / span 3;
  }
  The syntax is grid-row-start / grid-column-start / grid-row-end / grid-column-end.
Item1 will start on row 2 and column 1, and span 2 rows and 3 columns:
 */
</style>
