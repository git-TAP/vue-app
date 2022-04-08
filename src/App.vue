<template>
  <h1>DC Heroes</h1>
  <ul>
    <li  v-for="(hero, index) in dcHeroes" v-bind:key="index">{{ index }} : {{hero.name}}</li>
    <input type="text" v-model.lazy="newHero"> <!--Make newHero model -->
    <button>Add Hero</button>
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