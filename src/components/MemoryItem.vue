<template>
    <article class="memory-card">
        <div class="img-section">
            <img :src="memory.image" alt="image">
        </div>
        <div class="title">
            <p class="name" >{{ memory.name }}</p>
            <p class="date">10/02/2023</p>
        </div>

        <div class="memory-content">
            <h3>{{ memory.title }}</h3>
            <p>{{ memory.message }}</p>
        </div>

        <div class="tags-container">
            <template v-for="tag of memory.tags" :key="tag">
            <p class="tag">#{{ tag }}</p>
            </template>
        </div>

    </article>
</template>

<script>
export default {
  name: 'MemoryItem',
  props: {
    memory: Object
  }
}
</script>

<style scoped>
.memory-card {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    height: 100%;
    position: relative;
    width: 18rem;
    background-color: #fff;
    color: #000;
    border: 2px solid #000;
}
.title{
    display: flex;
    justify-content: space-between;
    align-items: baseline;
    padding: 0 10px;
}
img {
    height: 100%;
    width: 100%;
}
.img-section {
    height: 200px;
    width: 100%;
}
.name{
    font-weight: bold;
    color:black;
}
.date {
    font-size: 10px;
}
.tags-container {
    display: flex;
    flex-wrap: wrap;
    margin-top: 5px;
    padding: 5px 10px;
}
.tag {
    margin-right: 5px;
    font-size: 12px;
}
.memory-content{
    padding: 5px 10px;
}
.likes {
    padding: 10px;
    color: #4a4aff ;
}
.memory-content p {
    font-size: 13px;
}
.memory-content h3 {
    font-weight: bold;
}
</style>