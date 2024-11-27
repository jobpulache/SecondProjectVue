<template lang="">
  <h1>Example: 'v-bind:' shorthand form ':'.</h1>
  <p>Take a look at the div where the class is set with the 'v-bind:' shorthand form ':'.</p>
  <div id="app">
    <div :class="{ myClass: isImportant }">
      Importance visualized by background color
    </div>
  </div>
</template>

<script>
  export default {
    name: 'T03vbind',
    components : {},
    data() {
      return {
        isImportant: false
    }
   }
  }  
</script>

<style>
  .myClass {
    background-color: lightcoral;
  }
</style>