<template>
  <div id="app">
    <HomePage />
  </div>
</template>

<script>

import HomePage from './views/HomePage.vue';

export default {
  name: 'App',
  components: {
    HomePage,
  },
};
</script>

<style lang="scss">
#app {
text-align: center;
  color: deeppink;
  margin-top: 60px;
  font-family: Avenir,Helvetica,Arial,sans-serif;
  -webkit-font-smoothing: antialiased;
}
</style>
