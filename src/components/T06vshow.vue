<template>
  <div>
    <h1>Example: v-show Visibility of Div Element</h1>

    <div id="example06">
      <p>Find the 'showDiv' data property in the code, change it to 'false', and run the code again.</p>
      <div v-show="showDiv">This div tag can be hidden</div>
    </div>
  </div>
</template>
<script>
export default {
  name: 'T06vshow',
  components: {},
  data() {
    return {
      showDiv: true
    }
  }
}
</script>
<style lang="css">
  #example06 {
    border: black dashed 1px;
    width: 200px;
    padding: 0 20px 20px 20px;
  }
  #example06 div {
    padding: 20px;
    background-color: lightgreen;
    font-weight: bold;
  }
</style>