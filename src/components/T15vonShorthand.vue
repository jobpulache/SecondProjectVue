<template>
  <div>
    <h1>Example: v-on Shorthand '@'</h1>
    <p>With the v-on shorthand we can write '@:click' instead of 'v-on:click'.</p>
    <div id="app">
      <div id="lightDiv">
        <div v-show="lightOn"></div>
        <img src="../assets/img/img_lightBulb.svg">
      </div>
      <button @:click=" lightOn =! lightOn ">Switch light</button>
    </div>
  </div>
</template>
<script>
export default {
  name: '',
  components: {},
  data() {
    return {
      lightOn: false
    }
  }
}
</script>
<style lang="css">
  #app {
    border: dashed black 1px;
    display: inline-block;
    padding-bottom: 10px;
  }

  #app > button {
    display: block;
    margin: auto;
  }

  #lightDiv {
    position: relative;
    width: 150px;
    height: 150px;
  }

  #lightDiv > img {
    position: relative;
    width: 100%;
    height: 100%;
  }

  #lightDiv > div {
    position: absolute;
    top: 10%;
    left: 10%;
    width: 80%;
    height: 80%;
    border-radius: 50%;
    background-color: yellow;
  }
</style>