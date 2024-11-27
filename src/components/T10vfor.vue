<template>
  <div>
    <h1>Example: Get the array element index with 'v-for'</h1>
    <p>The 'v-for' directive is used to get the index of objects inside the 'manyFoods' array, together with the name and url of each food object.</p>

    <div id="app">
      <div>
        <p v-for="(item, index) in manyFoods">
          Index: "{{ index }}", name: "{{ item.name }}", url: "{{ item.url }}" <br>
        </p>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: 'T10vfor',
  components: {},
  data() {
    return {
      manyFoods: [
        {name: 'Burrito', url: 'src/assets/img/img_burrito.svg'},
        {name: 'Salad', url: 'src/assets/img/img_salad.svg'},
        {name: 'Cake', url: 'src/assets/img/img_cake.svg'},
        {name: 'Soup', url: 'src/assets/img/img_soup.svg'},
        {name: 'Fish', url: 'src/assets/img/img_fish.svg'},
        {name: 'Pizza', url: 'src/assets/img/img_pizza.svg'},
        {name: 'Rice', url: 'src/assets/img/img_rice.svg'}
      ]
    }
  }
}
</script>
<style lang="css">
  
</style>