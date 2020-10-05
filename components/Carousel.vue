<template>
  <div class="carousel-wrapper -mx-3">
    <hooper ref="carousel" style="height: auto" :settings="hooperSettings">
      <slide v-for="i in 4" :key="i">
        <div>
          <img :src="`./carousel/${i}.jpg`" />
        </div>
      </slide>
      <pagination
        slot="hooper-addons"
        :class="{ number: isNumberPage }"
        :mode="isNumberPage ? 'fraction' : 'indicator'"
      ></pagination>
    </hooper>
  </div>
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
  props: {
    isNumberPage: Boolean,
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
.carousel-wrapper :focus {
  outline: none !important;
}

.hooper-pagination {
  &.number {
    background: white;
    border-radius: 8px;
    color: #333333;
    right: 5%;
    bottom: 8px;
  }
}
</style>
