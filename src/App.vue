<template>
   <scrollbar :prototype="this.prototype"></scrollbar>
</template>

<script>

import NewsItem from "@/components/news-item";
import Scrollbar from "@/components/scrollbar";
import Scrollbar_v2 from "@/components/scrollbar_v2";
export default {
  name: 'App',
  components: {
    Scrollbar_v2,
    Scrollbar,
    NewsItem
  },
  data() {
    return {
      prototype: [
        {
          redaction: 'RT',
          header: 'Минобороны России опровергло фейк о якобы убийстве мирных жителей в Буче.',
          body: 'Министерство обороны России опровергло обвинения со стороны киевского режима в якобы убийстве мирных жителей в населённом пункте Буча Киевской области. Там напомнили, что мэр Бучи Анатолий Федорук 31 марта в своём видеообращении подтвердил, что в городе никого из российских военных нет, более того, он не упоминал о каких-либо «расстрелянных на улицах местных жителях со связанными руками».',
          link: '',
        },
        {
          redaction: 'rianews',
          header: 'В Буче произошел хорошо срежиссированный и чудовищный подлог, заявил Песков.',
          body: '"Мы по-прежнему настаиваем, что любые обвинения в адрес российской стороны, в адрес российских военных не просто являются беспочвенными, а это хорошо срежиссированное шоу. Ни что иное. Трагическое шоу", - сказал он журналистам.',
          link: '',
        },
        {
          redaction: 'Meduza',
          header: 'Как убивали людей в Буче. Подробная реконструкция событий. И разбор версий кремлевcкой пропаганды.',
          body: 'Съешь еще этих мягких французских булок, да выпей чаю...12345678900, Съешь еще этих мягких французских булок, да выпей чаю...12345678900',
          link: '',
        },
        {
          redaction: 'RadioSvoboda',
          header: 'Зеленский обвинил Россию в геноциде. Он побывал в Буче.',
          body: 'Президент Украины приехал в Бучу. Он назвал убийства мирных жителей геноцидом. Россия отвергает обвинения и заявляет, что кадры - постановка. Евроосюз заявил, что ответственность за убийства людей в Киевской области несут российские власти и готовит новые санкции против Москвы.',
          link: ''
        }
      ]
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}
html {
  background-color: white;
}
footer {

}
</style>
