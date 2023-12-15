<template>

    <div v-for="memory of memories" :key="memory.name">

        <MemoryItem :memory="memory" />

    </div>

</template>

<script>
import MemoryItem from './MemoryItem.vue'

export default {
  name: 'MemoriesList',
  components: {
    MemoryItem
  },

  props: {
    memories: Array
  }
}
</script>

<style scoped> 
    div {
        margin: 10px 20px;
    }
</style>