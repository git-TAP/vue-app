<template>
  <h1  v-text="count"></h1>  
  <span>Count is: {{count}}</span>
</template>


<script>
  export default{
    data(){    
      return{
        title:"<h1>This is the Title inside the H1 tag</h1>",
        isShowing: false,
        count:0,
      }
    },
    mounted(){
      setInterval(() => {
        this.count++;
      }, 1000)
    }
  }
</script>