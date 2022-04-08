<template>
  <h1>DC Heroes</h1>
  <ul>
    <li  v-for="(hero, index) in dcHeroes" v-bind:key="index">{{ index }} : {{hero.name}}</li>
    <input type="text" v-model.number="newHero"> <!--Make newHero model -->
    <button v-on:click="newHero = 'Wonder Woman'">Add Hero</button>
  </ul>
</template>


<script>
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