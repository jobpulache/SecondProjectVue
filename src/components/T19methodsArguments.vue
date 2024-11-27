<template>
  <div>
    <h1>Example: Passing Arguments with Methods</h1>

    <div id="example19">
      <img src="../assets/img/img_moose.jpg" width="233" height="233">
      <p>{{ "Moose count: " + count }}</p>
      <button v-on:click="addMoose(1)">+1</button>
      <button v-on:click="addMoose(5)">+5</button>
      <button v-on:click="addMoose(-1)">-1</button>
    </div>
  </div>
</template>
<script>
export default {
  name: 'T19methodsArguments',
  components: {},
  data() {
    return {
      count: 0
    }
  },
  methods: {
    addMoose(number) {
      this.count += number;
      /* the same as this.count=this.count+number */
    }
  }
}
</script>
<style lang="css">
  #example19 {
    border: dashed black 1px;
    width: 250px;
    padding: 10px;
  }
  #example19 > img {
    width: 100%;
  }
  button {
    margin: 10px;
    padding: 5px 10px;
  }
</style>