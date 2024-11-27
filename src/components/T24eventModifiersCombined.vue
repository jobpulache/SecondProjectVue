<template>
  <div>
    <h1>Example: 'S' and 'Ctrl' Combination Generates Alert</h1>

    <div id="example24">
      <p>Press 'Ctrl' and 'S' in combination to generate an alert:</p>
      <textarea cols="20" rows="3" v-on:keydown.ctrl.s="createAlert" placeholder="Start writing.."></textarea>
    </div>
  </div>
</template>
<script>
export default {
  name: '',
  components: {},
  data() {},
  methods: {
    createAlert(evt) {
      alert("You pressed the 'S' and 'Ctrl' keys, in combination!")
    }
  }
}
</script>
<style lang="css">
  #example24 {
    border: black dashed 1px;
    width: 200px;
    padding: 0 20px 20px 20px;
  }
  #example24 > div {
    width: 160px;
    background-color: lightcoral;
    padding: 20px;
  }
  #example24 span {
    color: black;
    font-weight: bold;
    font-family: 'Courier New', Courier, monospace;
  }
</style>