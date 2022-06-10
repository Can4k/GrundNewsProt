<template>
  <div class="news-container" :class="source.redaction">
    <img v-if="source.redaction === 'RT'" src="@/assets/logos/rt.png" :alt="source.redaction">
    <img v-if="source.redaction === 'Meduza'" src="@/assets/logos/meduza.png" :alt="source.redaction">
    <img v-if="source.redaction === 'rianews'" src="@/assets/logos/rianews.png" :alt="source.redaction">
    <img v-if="source.redaction === 'RadioSvoboda'" src="@/assets/logos/RadiosSvoboda.png" :alt="source.redaction">
    <div class="header-container">
      <strong>
        {{source.header}}
      </strong>
    </div>
    <div class="data-container">
      <p>
        {{source.body}}
      </p>
    </div>
    <button>ЧИТАТЬ ОРИГИНАЛ</button>
  </div>
</template>

<script>
export default {
  name: "news-item",
  props: {
    source: Object,
    position: Number
  }
}
</script>

<style scoped>
.news-container {
  width: 550px;
  min-height: 300px;
  border-radius: 10px;
  display: flex;
  align-items: flex-start;
  flex-direction: column;
  justify-content: flex-start;
  padding: 10px;
  margin: 5px;
  text-align: left;
}
.header-container {
  color: black;
  padding: 0 8px 8px 8px;
}
.data-container {
  color: black;
  padding: 8px;
}
p {
  font-family: Montserrat,serif;
  font-weight: 1000;
  font-size: 10px;
}
img {
  height: 70px;
}
button {
  padding: 10px;
  border-radius: 0;
  font-size: 12px;
  font-family: Montserrat,serif;
  font-weight: 1000;
  margin: 8px;
}
strong {
  font-size: 18px;
  font-family: Montserrat,serif;
  font-weight: 1000;
}
.RT {
  background-color: #77BC1F;
  text-align: left;
}
.RT button {
  background: #77BC1F;
  color: black;
  border: 1px solid black;
}
.Meduza {
  background-color: black;
  border: 1px solid burlywood;
}
.Meduza strong {
  font-size: 16px;
  color: burlywood;
}
.Meduza button {
  background-color: black;
  color: burlywood;
  border: 1px solid burlywood;
}
.Meduza p {
  font-family: Montserrat,serif;
  font-weight: 1000;
  color: burlywood;
}
.rianews {
  background-color: white;
  border: 1px solid darkblue;
}
.rianews img {
  height: 40px;
  margin: 10px;
  margin-bottom: 20px;
}
.rianews strong {
  font-size: 16px;
  color: darkblue;
}
.rianews button {
  background-color: white;
  color: darkblue;
  border: 1px solid darkblue;
}
.rianews p {
  font-family: Montserrat,serif;
  font-weight: 1000;
  color: darkblue;
}
.RadioSvoboda {
  border: 1px solid orange;
  background-color: white;
}
.RadioSvoboda button {
  border: 1px solid black;
  background-color: white;
  color: black;
}
</style>