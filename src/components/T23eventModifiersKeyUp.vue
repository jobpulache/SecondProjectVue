<template>
  <div>
    <h1>Example: Find The Keyboard Key Value</h1>

    <div id="example23">
      <p>Start writing inside the text box to record the key value:</p>
      <input type="text" v-on:keydown="getKey">
      <p id="green23">{{ keyValue }}</p>

      <p>Try pressing the 's' key:</p>
      <textarea v-on:keyup.s="createAlert"></textarea>
    </div>
  </div>
</template>
<script>
export default {
  name: '',
  components: {},
  data() {
    return {
      keyValue: ''
    }
  },
  methods: {
    getKey(event) {
      this.keyValue = event.key
      console.log(event.key)
    },
    createAlert() {
      alert("You pressed the 'S' key!")
    }
  }
}
</script>
<style lang="css">
  #example23 {
    border: black dashed 1px;
    width: 200px;
    padding: 0 20px 20px 20px;
  }
  #green23 {
    background-color: lightgreen;
  }
</style>