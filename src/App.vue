<template>
  <h1>DC Heroes</h1>
  <ul>
    <li  v-for="(hero, index) in dcHeroes" v-bind:key="index">{{ index }} : {{hero.name}}</li>
  </ul>
  <form action="" @submit.prevent="dcHeroes.push({name:newHero}); newHero =''">
     <input type="text" v-model="newHero" placeholder="Type your name here"> <!--Make newHero model -->
     <button type="submit">Add Hero</button>

  </form>
</template>


<script>
"use strict";
  export default{

    data(){    
      return{
       newHero:"Aquaman",
       dcHeroes: [
         {name:'Chocolate'},
         {name:'Factory'},
         {name:'power'}, 
         {name:'Superman'},
      ],
      }
    },
    mounted(){
      setInterval(() => {
        this.count++;
      }, 1000)
    }
  }
</script>