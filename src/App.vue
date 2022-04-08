<template>
  <h1 v-if="isShowing" v-html="title"></h1>
  <h2 v-else-if="isShowing == null">This is v-else-if part</h2>
  <h3 v-else>This is v-else part</h3>
  
</template>


<script>
  export default{
    data(){    
      return{
        title:"<h1>This is the Title inside the H1 tag</h1>",
        isShowing: false,
      }
    }
  }
</script>