<template>
  <div>
    <h1>Example: 'v-for' to create li-tags</h1>

    <p>In this example 'v-for' creates an 'li' tag with the food name for each food item in the Vue instance array.</p>

    <div id="example08">
      <ol>
        <li v-for="x in manyFoods">{{ x }}</li>
      </ol>
    </div>
  </div>
</template>
<script>
export default {
  name: 'T08vfor',
  components: {},
  data() {
    return {
      manyFoods: [
        'Burrito',
        'Salad',
        'Cake',
        'Soup',
        'Fish',
        'Pizza',
        'Rice'
      ]
    }
  }
}
</script>
<style lang="css">
  #example08 > div {
    border: solid black 1px;
    width: 20%;
    padding: 10px;


  }
</style>