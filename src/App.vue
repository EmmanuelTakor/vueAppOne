<template>
  <div>{{ greeting }}</div>
  <div v-text="sentence"></div>
  <div v-html="assuring"></div>
  <div v-bind:id="houseID">House</div>
  <button v-bind:disabled="isDisabled">Click</button>
  <div v-bind:class="underlineClass">Where are You?</div>
  <div v-bind:class="status">Status</div>
  <div v-bind:class="isPromoted && 'Promoted'">Promoted</div>
  <div v-bind:class="isSoldOut ? 'soldOut' : 'new'">SoldOut</div>
  <div v-if="gender === male">You are male</div>
  <div v-else>You are female</div>
  <template v-if="display">
    <h1>The Greatyest</h1>
    <h1>The Greatyest</h1>
    <h1>The Greatyest</h1>
  </template>
  <div v-for="name in names" :key="name">{{ name }}</div>
  <div v-for="film in films" :key="film">{{ film }}</div>
</template>
<script>
export default {
  name: "App",
  data() {
    return {
      greeting: "Hello",
      sentence: "How are you?",
      assuring: "<b>Are you certain?</b>",
      houseID: "houseOne",
      isDisabled: true,
      underlineClass: "underline",
      status: "failure",
      isPromoted: true,
      isSoldOut: true,
      gender: "female",
      display: false,
      names: ["James", "John", "Paul"],
      films: ["John The Thief", "BatMan", "Vice"],
    };
  },
};
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
.underline {
  text-decoration: underline;
}
.success {
  color: green;
}
.failure {
  color: red;
}
.Promoted {
  font-style: italic;
}
.soldOut {
  color: red;
  background: black;
}
.new {
  color: blue;
}
</style>
