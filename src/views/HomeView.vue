<script setup>
import HeaderTemplate from '../components/HeaderTemplate.vue';
import TournamentCard from '../components/TournamentCard.vue';
import {ref} from 'vue';

let tournaments = [
  {
    title: 'TFT tournament',
    imgName: 'tft.jpg'
  },
  {
    title: 'LOL tournament',
    imgName: 'lol.jpg'
  },
  {
    title: 'Valorant tournament',
    imgName: 'valorant.jpg'
  },
  {
    title: 'LOR tournament',
    imgName: 'lor.jpg'
  },
  {
    title: 'Valorant tournament',
    imgName: 'valorant.jpg'
  },
  {
    title: 'LOL tournament',
    imgName: 'lol.jpg'
  },
  {
    title: 'LOR tournament',
    imgName: 'lor.jpg'
  },

]

let nbToShow = ref(5);

let updateToShow = () => {
  nbToShow = 4
  console.log(nbToShow);
}

</script>

<template>

  <header>
    <div>
      <h1>Ewin</h1>
    </div>
    <div id="logLinks">
      <RouterLink class="nav" to="/signin">Sign in</RouterLink>
      <RouterLink class ="nav" to="/signup">Sign up</RouterLink>
    </div>
  </header>

  <main>
    <h2>Tournament's list</h2>
    <div class="showMoreDiv">
      <button class="button" @click="nbToShow = tournaments.length" >Show more</button>
    </div>
    <div class="cardContainer" >
      <TournamentCard v-for="i in nbToShow " :title="`${tournaments[i-1].title}`" :imgName="`${tournaments[i-1].imgName}`"/>
    </div>
  </main>

</template>

<style scoped>

  main{
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    margin : 2em
  }

  h1{
    font-size: 3em;
    font-weight: bold;
    color: hsla(160, 100%, 37%, 1);
  }

  h2{
    font-size: 2em;
    font-weight: bold;
    color :#EEEEEE
  }

  header {
    display: flex;
    width: 100%;
    height: 100px;
    padding: 4em 4em 2em 4em;
    justify-content: space-between;
    align-items: center;
    /*background: linear-gradient(45deg, #FF2E63, #08D9D6);*/
    /*background-color: hsla(160, 100%, 37%, 1);*/
    /*border-bottom: #EEEEEE 0.5px solid*/
  }

  #logLinks {
    display: flex;
    justify-content: space-evenly;
    width: 20%;
    font-size: 1.2em;
  }

  .showMoreDiv{
    margin-top: 2em;
    display: flex;
    justify-content: flex-end;
    width: 100%;
    padding-right: 16%;
  }

  .buttonShowMore{
    width: 8em;
    font-size: 1em;
    height: 2.5em;
    border-radius: 0.4em;
    margin-top: 1em;
    background-color: #EEEEEE;
    color: #393E46;
    border: hsla(160, 100%, 37%, 1) solid 1px;
    cursor: pointer; 
  }

  .cardContainer {
    margin-top: 3rem;
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: flex-start;
    align-content: center;
    margin-left: 15%;
    flex-wrap: wrap;
    gap : 5vw;
    width: 100%;
  }

  .nav {
    color: #EEEEEE;
    text-decoration: none;
  }

  .nav:hover {
    color: #EEEEEE;
    text-decoration: underline;
  }

</style>
