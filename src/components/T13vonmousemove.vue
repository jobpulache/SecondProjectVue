<template>
  <div>
    <h1>Example: Change Color</h1>

    <div id="example13">
      <p>Move the mouse pointer over the box below to change the background-color randomly with hsl color code.</p>
      <div @:mousemove=" colorVal = Math.floor(Math.random()*360) " :style=" {backgroundColor: 'hsl('+colorVal+',60%,60%)'} "></div>
      <p><span>backgroundColor: hsl(<strong>{{ colorVal }}</strong>, 80%, 80%)</span></p>
      <p>To understand how to set a color in CSS with 'hsl()' see <a href="/css/css_colors_hsl.asp" target="_blank">our page about this</a>.</p>
    </div>
  </div>
</template>
<script>
export default {
  name: '',
  components: {},
  data() {
    return {
      colorVal: 50
    }
  }
}
</script>
<style lang="css">
  #example13 {
    border: dashed black 1px;
    width: 350px;
    padding: 0 20px;
  }
  #example13 > div {
    width: 200px;
    height: 80px;
  }
  #example13 span {
    font-weight: bold;
    font-family: 'Courier New', Courier, monospace;
  }
</style>