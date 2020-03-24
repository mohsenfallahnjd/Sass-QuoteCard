<template>
  <div id="app">
    <Card />
  </div>
</template>

<script>
import Card from "./components/Card";

export default {
  name: "App",
  components: {
    Card
  }
};
</script>

<style lang="sass">

*
  margin: 0
  box-sizing: border-box

body
  background: linear-gradient( to bottom right ,#60606c, #18171d )
  background-repeat: no-repeat
  background-size: cover

#app
  display: flex
  justify-content: center
  align-items: center
  height: 100vh
</style>
