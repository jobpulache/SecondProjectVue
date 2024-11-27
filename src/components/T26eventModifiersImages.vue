<template>
  <div>
    <h1>Example</h1>

    <div id="example26">
      <p>Press the 'Shift' keyboard key while you do a left mouse button click on the image below to change it.</p>
      <img v-on:click.left.shift="changeImg" v-bind:src="imgUrl">
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      imgUrlIndex : 0,
      imgUrl: 'src/assets/img/img_tiger_square.jpeg',
      images: [
        'src/assets/img/img_tiger_square.jpeg',
        'src/assets/img/img_moose.jpg',
        'src/assets/img/img_kangaroo_square.jpeg'
      ]
    }
  },
  methods: {
    changeImg() {
      this.imgUrlIndex++;
      if(this.imgUrlIndex>=3){
        this.imgUrlIndex=0
      }
      this.imgUrl = this.images[this.imgUrlIndex]
    }
  }
}
</script>
<style lang="css">
  #example26 {
    border: black dashed 1px;
    width: 200px;
    padding: 20px;
  }
  #example26 > img {
    width: 100%;
  }
</style>