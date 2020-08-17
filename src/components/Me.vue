<template>
  <div>
    <div class="grid-container">
      <div class="profile-data">
        <h2><div class="roundedImage"></div>Profile</h2>
        <br/>
        <span class="inline-group"><h4>Name: </h4> <div>{{name}}</div> </span>
        <span class="inline-group"><h4>Klasse: </h4> <div>{{heroClass}}</div> </span>
        <p>Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s when an unknown printer took a galley of type and scrambled it to make a type specimen book.</p>
        <br/>
        <v-btn color="green" @click="remindOfSuccess()">Success!</v-btn>
      </div>
      <div class="quest-data primary-light-bg"><h4>Your Quests:</h4>
      <ol>
        <li v-for="questItem in quests" :key="questItem.title"> 
          <h5>{{questItem.title}}</h5>
          <p>{{questItem.description}} </p> 
          <div>{{questItem.dueDate}}</div> 
        </li>
      </ol>
      
      </div>
      <div class="side-quest-data secondary-cl-bg white-cl">Side quest data,  It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum</div>  
      <div class="hero-image secondary-light-bg"><img src="./../assets/warriorprincess.jpg"  height="580px" width="330px"></div>
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
  heroClass: string = 'Wallküre';
  quest: Object = { title: 'Finish my first jira ticket', description: 'work out what is missing', dueDate: '1 week', party: 'Blueend', fellows: 'Stefan'}; 
  quests: Object[] = [];

  remindOfSuccess() {
    this.levelCount++;
    this.quests.push(this.quest);
    console.log("Level count", this.levelCount)
    alert("Wow, you went up 1 level! That's now at Level " + this.levelCount + "!")
  }
}
</script>

<style scoped lang="scss">

  .grid-container {
    display: grid;
    grid-gap: 20px;
    grid-template-columns: 1fr 2fr;
    grid-template-rows: 2fr 0.5fr 0.5fr 1fr 2fr;
  }

  .profile-data {
    grid-area: 1 / 1 / span 1 / span 1;
    padding: 20px 25px 20px 25px;
  }
 
  .quest-data {
    grid-area: 2 / 1 / span 1 / span 1;
    padding: 20px 25px 15px 15px;
  }

  .side-quest-data {
    grid-area: 3 / 1 / span 1 / span 1;
    padding: 20px 25px 15px 15px;
  }
  .hero-image {
     grid-area: 1 / 2 / span 3 / span 1;
     display: flex;
     flex-direction: column;
     justify-content: center;
  }

  .inline-group {
    display: flex;
    flex-direction: row;
    justify-content: flex-start;
    
    div {
      margin-left: 10px;
    }
  }

  .roundedImage {
    background: url('./../assets/warriorqueen.jpg');
    background-repeat: no-repeat;
    background-size: cover;
    
    overflow:hidden;
    -webkit-border-radius:50px;
    -moz-border-radius:50px;
    border-radius:50px;
    width:90px;
    height:90px;
  }
  
  /**
  .item1 {
    grid-area: 2 / 1 / span 2 / span 3;
  }
  The syntax is grid-row-start / grid-column-start / grid-row-end / grid-column-end.
Item1 will start on row 2 and column 1, and span 2 rows and 3 columns:
 */
</style>
