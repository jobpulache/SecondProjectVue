<template>
  <div>
    <h1>Example: Right Mouse Button Event</h1>

    <div id="example25">
      <div 
        v-on:click.right="changeColor1" 
        v-bind:style="{ backgroundColor:'hsl('+bgColor1+',80%,80%)' }"
      >
        <p>Press right mouse button here.</p>
      </div>

      <div 
        v-on:click.right.ctrl="changeColor2"
        v-bind:style="{backgroundColor:'hsl('+bgColor2+',80%,80%)'}"
      >
        <p>Press right mouse button here.</p>
      </div>
      <div 
        v-on:click.right.prevent="changeColor3"
        v-bind:style="{backgroundColor:'hsl('+bgColor3+',80%,80%)'}"
      >
        <p>Press right mouse button here.</p>
      </div>

    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      bgColor1 : 0,
      bgColor2 : 0,
      bgColor3 : 0
    }
  },
  methods: {
    changeColor1() {
      this.bgColor1+=50;
    },
    changeColor2() {
      this.bgColor2+=50
    },
    changeColor3() {
      this.bgColor3+=50
    }
  }
}
</script>
<style lang="css">
  #example25 {
    border: black dashed 1px;
    width: 200px;
    padding: 20px;
  }
  #example25 > div {
    width: 160px;
    padding: 20px;
    cursor: default;
    font-weight: bold;
  }
</style>