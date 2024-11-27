<template>
  <div>
    <h1>Example 'v-for' to create images and text</h1>
    <p>The 'v-for' directive is used to create images and text based on the 'manyFoods' array in the Vue instance.</p>
    <div id="example09">
      <div>
        <figure v-for="item in manyFoods">
          <img :src="item.url">
          <figcaption>{{ item.name }}</figcaption>
        </figure>
      </div>     
    </div>
  </div>
</template>
<script>
export default {
  name: '',
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
  #example09 > div {
    border: solid black 1px;
    width: 80%;
    padding: 10px;
    display: flex;
    flex-wrap: wrap;
    justify-content: space-around;
  }

  figure {
    width: 80px;
    padding: 10px;
    margin: 10px;
    background-color: lightskyblue;
    border-radius: 5px;
  }

  figcaption {
    text-align: center;
  }

</style>