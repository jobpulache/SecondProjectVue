<template>
  <div>
    <h1>Example: Passing an Argument and the Event Object with a Method</h1>
    <p>In this example we see that it is possible to send both the event object and a text as an argument with a method. To do this we must use the reserved name for event methods: '$event'.</p>
    <p>Click on the tiger image:</p>
    <div id="example20">
      <img src="../assets/img/img_tiger_square.jpeg" id="tiger" v-on:click="myMethod($event,'Hello')" width="233" height="233">
      <p>Here is the message sent with the method, and the id of the img tag:</p>
      <p id="green20">"{{ msgAndId }}"</p>
    </div>
  </div>
</template>
<script>
export default {
  name: 'T20methodsArgumentsObjects',
  components: {},
  data() {
    return {
      msgAndId: ''
    }
  },
  methods: {
    myMethod(e, msg) {
      this.msgAndId = msg + ', '
      this.msgAndId += e.target.id
    }
  }
}
</script>
<style lang="css">
  #example20 {
    border: dashed black 1px;
    width: 250px;
    padding: 10px;
  }
  #example20 img {
    width: 100%;
  }
  #green20 {
    background-color: lightgreen;
    display: inline-block;
  }
</style>