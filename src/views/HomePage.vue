<template>
  <div>
    <img src="./../assets/Quote.jpg" alt="quote" class="logo">
    <h1>Quote For The Day</h1>
    <button type="button" @click="quote">Click me for a Quote</button>
    <p>{{clickvalue}}</p>
  </div>
</template>

<script>
export default {
  name: 'HomePage',
  data() {
    return {
      clickvalue: '',
    };
  },
  methods: {
    quote() {
      this.clickvalue = 'I am clicked';
    },
  },
};
</script>

<style scoped>
  .logo {
    width: 10%;
  }

  img {
    vertical-align: middle;
  }

  button {
    background-color: deeppink;
    text-align: center;
    font-family: Avenir;
    font-size: larger;
    padding: 10px;
    border-radius: 30px;
    border-width: thick;
    border-color: pink;
    outline: none;
  }
</style>
