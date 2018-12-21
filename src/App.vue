<template>
  <div id="app">
    <img src="./assets/logo.png">
    <router-view/>
  </div>
</template>

<script>
export default {
  name: 'App',
  created () {
    this.$http('/apis/test', {
      params: {
        fild: 1,
        fild2: 2,
        file3: 3
      }
    }).then(function (response) {
      console.log(response)
    }).catch(function (error) {
      console.log(error)
    })
  }
}
</script>

<style lang="scss">
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  font-size: 0.02rem;
}
</style>
