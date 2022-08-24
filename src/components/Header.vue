<template lang="pug">
.header(:style="{backgroundImage: `url(${bg})`}")
  .name {{title}}
  img.avatar(:src="avatar")
</template>
<script setup name="Header">
import { title, avatar, bg } from '../config'
// data

// computed
// methods
// config
// lifecycle
</script>
<style lang="stylus" rel="stylesheet/stylus" scoped>
.header {
  position relative
  top 0
  width 100%
  height 300px
  background no-repeat center/cover
  .name {
    position absolute
    bottom 0
    color #fff
    right 100px
    font-size 28px
    text-shadow: 2px 2px 10px #000
  }
  .avatar {
    position absolute
    bottom -12px
    right 12px
    width 72px
    height 72px
    border-radius 4px
  }
}
</style>
