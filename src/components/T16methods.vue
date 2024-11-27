<template>
  <div>
    <h1>Example: Click to run a method</h1>

    <div id="example16">
      <p>Click on the box below:</p>
      <div v-on:click="changeText">
        {{ text }}
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: 'T16methods',
  components: {},
  data() {
    return {
      text: 'default text'
    }
  },
  methods: {
    changeText() {
      this.text = 'Hello World!'
    }
  }
}
</script>
<style lang="css">
  #example16 {
    border: black dashed 1px;
    width: 200px;
    padding: 0 20px 20px 20px;
  }
  #example16 > div {
    width: 140px;
    height: 60px;
    background-color: lightgreen;
    padding: 20px;
    font-weight: bold;
    font-family: 'Courier New', Courier, monospace;
  }
</style>