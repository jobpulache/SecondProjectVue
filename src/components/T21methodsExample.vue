<template>
  <div>
    <h1>Example: Passing Arguments and Event Object with Methods</h1>
    <p>In this example we are able to count tigers, moose and kangaroos, with different increments, all buttons refering to the same method. This is possible by passing the numbers counted as an argument, and by passing the event.</p>
    <div id="example21">
      <div id="tigers">
        <img src="../assets/img/img_tiger_square.jpeg" width="233" height="233">
        <button v-on:click="addAnimal($event,1)">+1</button>
        <button v-on:click="addAnimal($event,5)">+5</button>
        <button v-on:click="addAnimal($event,-1)">-1</button>
      </div>
      <div id="moose">
        <img src="../assets/img/img_moose.jpg" width="233" height="233">
        <button v-on:click="addAnimal($event,1)">+1</button>
        <button v-on:click="addAnimal($event,5)">+5</button>
        <button v-on:click="addAnimal($event,-1)">-1</button>
      </div>
      <div id="kangaroos">
        <img src="../assets/img/img_kangaroo_square.jpeg" width="233" height="233">
        <button v-on:click="addAnimal($event,1)">+1</button>
        <button v-on:click="addAnimal($event,5)">+5</button>
        <button v-on:click="addAnimal($event,-1)">-1</button>
      </div>
      <ul>
        <li>Tigers: {{ tigers }}</li>
        <li>Moose: {{ moose }}</li>
        <li>Kangaroos: {{ kangaroos }}</li>
      </ul>
    </div>
  </div>
</template>
<script>
export default {
  name: '',
  components: {},
  data() {
    return {
      tigers: 0,
      moose: 0,
      kangaroos: 0
    }
  },
  methods: {
    addAnimal(e,number) {
      if(e.target.parentElement.id==="tigers"){
        this.tigers+=number;
      }
      else if(e.target.parentElement.id==="moose"){
        this.moose+=number;
      }
      else{
        this.kangaroos+=number;
      }
    }
  }
}
</script>
<style lang="css">
  #example21 {
    border: dashed black 1px;
    box-sizing: border-box;
    padding: 10px;
    display: flex;
    flex-wrap: wrap;
  }
  #example21 > div {
    flex-basis: 200px;
    margin: 5px;
  }
  #example21 > img {
    width: 100%;
  }
  #example21 > button {
    margin: 5px;
    padding: 3px 6px;
  }
</style>