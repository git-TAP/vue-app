<template>
  <h1>DC Heroes</h1>
  <ul>
    <li  v-for="(hero, index) in dcHeroes" v-bind:key="index">{{ index }} : {{hero.name}}</li>
  </ul>
  <form action="" @submit.prevent="addHero">
     <input type="text" v-model="newHero" placeholder="Type your name here"> <!--Make newHero model -->
     <button type="submit" @disabled="disabled == 1" >Add Hero</button>

  </form>
</template>


<script>
"use strict";
  export default{
    methods:{
      addHero() {
        if(this.newHero != ""){
          this.dcHeroes.push({name:this.newHero});
          this.newHero = "";
        }
        
      },
    },

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