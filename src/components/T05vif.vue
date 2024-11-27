<template>
  <h1>Example with text check</h1>

  <p>In this example 'v-if' uses a method 'includes()' instead of a comparison operator.</p>

  <p>Remove 'pizza' from the 'text' property inside the Vue instance, click 'Run' and see what happens.</p>

  <div id="example05">
    <div v-if="text.includes('pizza')">
      <p>The text includes the word 'pizza'</p>
      <img src="https://picsum.photos/200/100">
    </div>
    <p v-else>The word 'pizza' is not found in the text</p>
  </div>
</template>
<script>
export default {
  name: "T05vif",
  components: {},
  data() {
    return {
      text: 'I like taco, Thai beef salad, pho soup and tagine.'
    }
  }
}
</script>
<style lang="css">
  #example05 {
    border: dashed black 1px;
    width: 160px;
    padding: 0 20px;
    font-weight: bold;
    background-color: lightgreen;
  }
</style>