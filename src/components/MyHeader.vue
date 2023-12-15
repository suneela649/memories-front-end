<template>
    <header>
       <h1>{{ AppName }}</h1> 
    </header>
</template>

<script>
export default {
  name: 'MyHeader',
  props: {
    AppName: String
  }
}
</script>


<style scoped>
    header {
    background-color: burlywood;
    height: 50px;
    text-align: center;
    display: flex;
    justify-content: center;
    align-items: center;
    }
    h1 {
        font-weight: bold;
        padding: 5px 0;
    }
</style>