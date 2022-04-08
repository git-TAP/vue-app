<template>
  <h1>DC Heroes</h1>
  <ul>
    <li  v-for="(hero, index) in dcHeroes" v-bind:key="index">{{ index }} : {{hero.name}}</li>
    <input type="text" v-bind:value="newHero">
    <button v-bind:disabled="isDisabled">Add Hero</button>
  </ul>
</template>


<script>
  export default{
    data(){    
      return{
       isDisabled: true,
       newHero:'Aquaman',
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