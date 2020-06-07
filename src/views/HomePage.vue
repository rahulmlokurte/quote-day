<template>
  <div>
    <h1>AWESOME BUTTON</h1>
    <button type="button" @click="quote"
            class="glow-on-hover"
    >Hover over Me and then Press and Hold Me</button>
  </div>
</template>

<script>
export default {
  name: 'HomePage',
  data() {
    return {
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

  h1 {
  color: deeppink;
    padding-bottom: 30px;
    font-family: cursive;
  }

  .glow-on-hover {
    text-align: center;
    font-family: cursive;
    font-size: 40px;
    padding: 30px;
    border-radius: 10px;
    border-width: thin;
    border-color: deeppink;
    outline: none;
    color: deeppink;
    cursor: pointer;
    box-shadow: 9px 9px deeppink;
    position: relative;
    z-index: 0;
  }

  .glow-on-hover:before {
    content: '';
    background: linear-gradient(45deg, #ff0000, #ff7300, #fffb00,
    #48ff00, #00ffd5, #002bff, #7a00ff, #ff00c8, #ff0000);
    position: absolute;
    top: -2px;
    left:-2px;
    background-size: 400%;
    z-index: -1;
    filter: blur(5px);
    width: calc(100% + 4px);
    height: calc(100% + 4px);
    animation: glowing 20s linear infinite;
    opacity: 0;
    transition: opacity .3s ease-in-out;
    border-radius: 10px;
  }

  .glow-on-hover:active {
    color: #000
  }

  .glow-on-hover:active:after {
    background: transparent;
  }

  .glow-on-hover:hover:before {
    opacity: 1;
  }

  .glow-on-hover:after {
    z-index: -1;
    content: '';
    position: absolute;
    width: 100%;
    height: 100%;
    background: #111;
    left: 0;
    top: 0;
    border-radius: 10px;
  }

  @keyframes glowing {
    0% { background-position: 0 0; }
    50% { background-position: 400% 0; }
    100% { background-position: 0 0; }
  }
</style>
