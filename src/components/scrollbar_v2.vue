<template>
  <section class="range">
  </section>
  <news-item class="leningrad" :style="top + left" :source="prototype[0]"/>
</template>

<script>
import NewsItem from "@/components/news-item";
import {useMouse} from '@vueuse/core'

const {x, y} = useMouse();

export default {
  name: "scrollbar_v2",
  components: {NewsItem},
  props: {
    prototype: Array
  },
  data() {
    return {
      x: x,
      y: y,
    }
  },
  computed: {
    top() {
      return "top: " + String(this.y) + "px;";
    },
    left() {
      return "left: " + String(this.x) + "px;";
    }
  }
}
</script>

<style scoped>
.range {
  display: flex;
  align-items: center;
  justify-content: space-around;
}
.leningrad {
  position: absolute;
}
</style>