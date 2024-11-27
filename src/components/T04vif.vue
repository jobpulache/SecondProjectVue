<template>
  <div>
    <h1>Example with 'v-if' and 'v-else'</h1>

    <p>Try changing the 'typewritersInStock' value in the Vue instance from 'true' to 'false' and run the code again.</p>

    <div id="example04">
      <p v-if="typeWritersInStock">
        in stock
      </p>
      <p v-else>
        not in stock
      </p>

      <p v-if="typeWriterCount > 0">
        It's greater than zero.
      </p>
      <p v-else>
        It's less than zero or equal to zero.
      </p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'T04vif',
  components : {},
  data() {
    return {
      typeWritersInStock: false,
      typeWriterCount: 0
    }
  }
}
</script>

<style lang="css">
  #example04 {
    border: dashed black 1px;
    width: 130px;
    padding-left: 20px;
    font-weight: bold;
    background-color: lightgreen;
  }
</style>