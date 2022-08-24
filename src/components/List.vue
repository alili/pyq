<template lang="pug">
.list
  .years(v-for="([year, items]) in years")
    span {{year}}
    Item(v-for="(item) in items"
      :="item")
</template>
<script setup name="List">
import { computed } from 'vue'
import Item from './Item.vue'
import { timeline } from '../config'

// data
// computed
const years = computed(() => {
  return Object.entries(timeline).sort(([a], [b]) => b - a)
})
// methods
// config
// lifecycle
</script>
<style lang="stylus" rel="stylesheet/stylus" scoped>
.list {
  margin 20px
  .years span {
    display inline-block
    font-weight bold
    margin-bottom 30px
    margin-left 4px

  }
}
</style>
