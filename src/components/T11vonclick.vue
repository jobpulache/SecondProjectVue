<template>
  <div>
    <h1>Example: Light Switch</h1>
    <p>The v-on directive is used on the button tag to listen to the 'click' event. When the 'click' event occurs the 'lightOn' data property is toggled between 'true' and 'false', making the yellow div behind the lightbulb visible/hidden.</p>
    <div id="example11">
      <div id="lightDiv">
        <div v-show="lightOn"></div>
        <img src="../assets/img/img_lightBulb.svg">
      </div>
      <button v-on:click=" lightOn =! lightOn ">Switch light</button>
    </div>
  </div>
</template>
<script>
export default {
  name: 'T11von',
  components: {},
  data(){
    return {
      lightOn: false
    }
  }
}
</script>
<style lang="css">
  #example11 {
    border: dashed black 1px;
    display: inline-block;
    padding-bottom: 10px;
  }

  #example11 > button {
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