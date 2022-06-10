<template>
  <news-item v-for="s in prototype" class="leningrad" :source="s"/>
</template>

<script>
import NewsItem from "@/components/news-item";
import {useMouse} from '@vueuse/core'

const {x, y} = useMouse()

export default {
  name: "scrollbar_v2",
  components: {NewsItem},
  props: {
    prototype: Array
  },
  data() {
  },
  computed: {

  }
}
</script>

<style scoped>
.range {
}
</style>