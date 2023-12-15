<template>
  <MyHeader AppName="MEMORIES APP" />
  <div class="container">
    <MemoriesList :memories="memories" />
  </div>
</template>

<script>
import MyHeader from './components/MyHeader.vue'
import MemoriesList from './components/MemoriesList.vue'

 export default {
  name: 'App',

  components:{
    MyHeader,
    MemoriesList
  },

  data(){
    return {
      memories: []
    }
  },

  methods:{
    async fetchMemories(){
      const res = await fetch('https://memories-app-backend-pe4h.onrender.com/api');
      const data = await res.json()
      console.log(data)
      return data
    }
  },

  async created(){
      this.memories = await this.fetchMemories();
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
.container {
  display: flex;
  flex-wrap: wrap;
}
html {
  margin: 0;
    background-color: antiquewhite;

}
</style>
