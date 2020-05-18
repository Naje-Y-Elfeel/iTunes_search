<template>
  <div>
    <h1>Search iTunes Now</h1>
    <br/>

    <form v-on:submit.prevent="submit">
      <input type="text" placeholder="Enter Artist Name" v-model="search" autofocus>
    </form>
    
  </div>
</template>

<script>
export default {
  data(){
    return{
      search: ''
    }
  },
  methods: {
    submit(){
      this.$router.push('results/'+this.search);
    }    
  }
}
</script>

<style>
*{
  text-align: center;
}
h1{
  padding: 20px;
}
</style>