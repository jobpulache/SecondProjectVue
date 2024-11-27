<template>
  <div>
    <h1>Example: Create Alert Only Once</h1>

    <div id="example22">
      <p>The button below creates an alert in a pop-up box, but only on the first click:</p>
      <button v-on:click.once="createAlert">Create Alert</button>
    </div>
  </div>
</template>
<script>
export default {
  name: '',
  components: {},
  data() {},
  methods: {
    createAlert() {
      alert("Alert created from button click")
    }
  }
}
</script>
<style lang="css">
  #example22 {
    border: black dashed 1px;
    width: 200px;
    padding: 0 20px 20px 20px;
  }
</style>