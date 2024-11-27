<script>
  export default {
    name: 'T01vbind',
    components : {},
    data() {
      return {
        myUrl: "https://picsum.photos/300/200",
        size: "24px",
        class: "myClassName2"
    }
   }
  }  
</script>

<template lang="">
  <div v-bind:class="class">
    <div v-bind:style="{ fontSize: size }">
      <p>The browser finds the 'src' attribute value from the Vue instance with the use of 'v-bind'.</p>
      <img v-bind:src="myUrl">
    </div>
  </div>
</template>

<style>
  .myClassName1{
    background-color: red;
  }
  .myClassName2{
    background-color: green;
  }
</style>