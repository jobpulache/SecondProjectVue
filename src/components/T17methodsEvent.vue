<template>
  <div>
    <h1>Example: Mouse Pointer Position</h1>

    <div id="example17">
      <p>Move the mouse pointer over the box below:</p>
      <div v-on:mousemove="mousePos" v-bind:style="{backgroundColor:'hsl('+xPos+',80%,80%)'}">
        <br><span>xPos: {{ xPos }}</span><br><span>yPos: {{ yPos }}</span>
      </div>
      <p>CSS:<br>backgroundColor:'hsl(<strong>{{xPos}}</strong>,80%,80%)'</p>
      <p>To understand how to set a color in CSS with 'hsl()' see <a href="/css/css_colors_hsl.asp" target="_blank">our page about this</a>.</p>
    </div>
  </div>
</template>
<script>
export default {
  name: 'T17methodsEvent',
  components: {},
  data() {
    return {
      xPos: 0,
      yPos: 0
    }
  },
  methods: {
    mousePos(event) {
      this.xPos = event.offsetX
      this.yPos = event.offsetY
    }
  }
}
</script>
<style lang="css">
  #example17 {
    border: black dashed 1px;
    width: 200px;
    padding: 0 20px 20px 20px;
  }
  #example17 > div {
    width: 160px;
    height: 80px;
    background-color: lightcoral;
    padding: 20px;
  }
  #example17 span {
    font-weight: bold;
    font-family: 'Courier New', Courier, monospace;
  }
</style>