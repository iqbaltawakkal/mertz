<template>
  <hooper ref="carousel" style="height: auto" :settings="hooperSettings">
    <slide v-for="i in 4" :key="i">
      <div>
        <img :src="`./carousel/${i}.jpg`" />
      </div>
    </slide>
    <pagination slot="hooper-addons"></pagination>
  </hooper>
</template>

<script>
import { Hooper, Slide, Pagination } from 'hooper'
import 'hooper/dist/hooper.css'

export default {
  name: 'Div',
  components: {
    Hooper,
    Slide,
    Pagination,
  },
  data() {
    return {
      hooperSettings: {
        itemsToShow: 1,
        itemsToSlide: 1,
        infiniteScroll: 1,
      },
    }
  },
}
</script>

<style lang="scss">
li:focus,
button:focus {
  outline: none;
}
</style>
