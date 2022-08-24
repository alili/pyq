<template lang="pug">
.item
  .day
    span.date {{dayjs(date).format('DD')}}
    span.month {{dayjs(date).format('M月')}}
  img.img(:src="img")
  .title {{title}}
</template>
<script setup name="Item">
import dayjs from 'dayjs'
const props = defineProps({
  date: {
    type: String,
    default: '',
  },
  title: {
    type: String,
    default: '',
  },
  img: {
    type: String,
    default: '',
  },
})
// data
// computed
// methods
// config
// lifecycle
</script>
<style lang="stylus" rel="stylesheet/stylus" scoped>
.item {
  display flex
  margin-bottom 30px
  .day {
    min-width 80px
    .date {
      font-size: 32px
      color: #000
      font-weight bold
      margin-right 4px
    }
    .month {
      font-size: 16px
      color: #000
      font-weight bold
    }
  }
  .img {
    width 100px
    height 100px
    margin-left 20px
    margin-right 10px
  }
  .title {
    font-size 16px
  }
}
</style>
