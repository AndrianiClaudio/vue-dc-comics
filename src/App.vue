<template>
  <div id="app">
    <div id='container'>
      <Header />
    </div>
  </div>
</template>

<script>
import Header from './components/Header.vue'

export default {
  name: "App",
  components: {
    Header,
  },
};
</script>

<style lang="scss">
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
#container {
  width: 80%;
  margin: 0 auto;
}
</style>
