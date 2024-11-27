<template>
  <div>
    <h1>Example: v-show vs. v-if</h1>

    <div id="example07">
      <p>Set the 'showDiv' data property to 'false', and run the code again. Right click this green p element, choose 'Inspect' or 'Inspect element' and you can see that the div element with v-show still exist, it is only the CSS display property that is set to 'none', and the div with v-if is destroyed.</p>
      <div v-show="showDiv">Div tag with v-show</div>
      <div v-if="showDiv">Div tag with v-if</div>
    </div>
  </div>
</template>
<script>
export default {
  name: 'T07vshow',
  components: {},
  data() {
    return {
      showDiv: true
    }
  }

}
</script>
<style lang="css">
  #example07 {
    border: black dashed 1px;
    width: 80%;
    padding: 0 20px 20px 20px;
  }
  #example07 div {
    padding: 20px;
    margin: 10px;
    display: inline-block;
    font-weight: bold;
    border: solid black 1px;
  }
  #example07 p {
    padding: 10px;
    background-color: rgb(200, 246, 200);
  }
</style>