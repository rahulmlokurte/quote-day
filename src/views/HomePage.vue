<template>
  <div>
    <h1>Quote For The Day</h1>
    <button type="button" @click="quote">Click me for a Quote</button>
    <p v-for="qu in quotes" v-bind:key="qu">{{qu}}</p>
  </div>
</template>

<script>
export default {
  name: 'HomePage',
  data() {
    return {
      clickvalue: '',
      quotes: [],
    };
  },
  methods: {
    quote() {
      this.clickvalue = 'I am clicked';
      this.quotes.push('My First Quote');
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
    text-align: center;
    font-family: cursive;
    font-size: 40px;
    padding: 30px;
    border-radius: 50%;
    border-width: thin;
    border-color: deeppink;
    outline: none;
    color: deeppink;
    cursor: pointer;
    box-shadow: 9px 9px deeppink;
    -webkit-animation: rotation infinite 5s;
  }

  @-webkit-keyframes rotation {
      from {
-webkit-transform: rotate(0deg);
      }
    to {
-webkit-transform: rotate(359deg);
    }
  }
  button:hover {
    background-color: yellow;
  }
  button:active {
box-shadow: 0 5px darkgreen;
    transform: translateY(4px);
  }

  h1 {
  color: deeppink;
    padding-bottom: 30px;
  }
</style>
