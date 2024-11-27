<template lang="">
  <div>
    <h1>Example: Show Food Image</h1>

    <p>Click on a food name below to see an image of it.</p>

    <div id="example14">
      <img :src="imgUrl">
      <ol>
        <li v-for="item in manyFoods" @:click="imgUrl = item.url">
          {{ item.name }}
        </li>
      </ol>
    </div>
  </div>
</template>
<script>
export default {
  name: '',
  components: {},
  data(){
    return {
      imgUrl: 'src/assets/img/img_pizza.svg',
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
  #example14 {
    border: dashed black 1px;
    width: 220px;
    padding: 20px;
  }

  #example14 > img {
    float: right;
    width: 55%;
  }

  #example14 li:hover {
    cursor: pointer;
    background-color: rgb(224, 224, 224);
  }

  #example14 > ol {
    list-style-type: none;
    margin: 0;
    padding: 0;
  }

  #example14 li {
    padding-left: 6px;
    border-radius: 5px;
    width: 70px;
  }
</style>