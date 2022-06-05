<template>
  <section class="range">
    <news-item :style="[+activeIndex - 1 >= 0 ? 'opacity: 1' : 'opacity: 0']" class="left" :source="prototype[Math.max(+activeIndex - 1, 0)]"></news-item>
    <news-item class="center" :source="prototype[activeIndex]"></news-item>
    <news-item :style="[+activeIndex + 1 < this.prototype.length ? 'opacity: 1' : 'opacity: 0']" class="right" :source="prototype[Math.min(+activeIndex + 1, prototype.length - 1)]"></news-item>
  </section>
  <div class="range">
    <strong>ГОСУДАРСТВЕННЫЕ</strong>
    <input @click="log()" type="range" min="0" :max="prototype.length - 1" v-model="activeIndex">
    <strong>ИНОАГЕНТЫ</strong>
  </div>
</template>

<script>
import NewsItem from "@/components/news-item";
export default {
  name: "scrollbar",
  components: {NewsItem},
  props: {
    prototype: Array
  },
  data() {
    return {
      activeIndex: 1
    }
  },
  mounted() {
    this.activeIndex = Math.floor(this.prototype.length / 2);
  },
  methods: {
    log() {
      console.log(this.activeIndex);
    }
  }
}
</script>

<style scoped>
.range {
  display: flex;
  align-items: center;
  justify-content: center;
  background-color: black;
  padding: 5px;
}
.left {
  transform: scale(0.8);
}
.right {
  transform: scale(0.8);
}
strong {
  font-family: Montserrat, sans-serif;
  font-weight: 1000;
  font-size: 10px;
  margin: 0px 10px 0 10px;
  color: white;
}
</style>