<template>
  <div>
    <h1>Example: Notebook</h1>

    <div id="example18">
      <textarea v-on:input="writeText" rows="8" cols="30" placeholder="Start writing.."></textarea>
      <div>
        <span>{{ text }}</span>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: 'T18methodsTextArea',
  components: {},
  data() {
    return {
      text: ''
    }
  },
  methods: {
    writeText(event) {
      this.text = event.target.value
    }
  }
}
</script>
<style lang="css">
  #example18 {
    border: black dashed 1px;
    width: 300px;
    padding: 20px;
  }
  #example18 > div {
    width: 100%;
    position: relative;
    margin-top: 10px;
    aspect-ratio: 1;
    background-image: url("src/assets/img/img_notebook.jpg");
    background-size: 340%;
    background-position: -345px 0;
    overflow: hidden;
  }
  #example18 span {
    width: 80%;
    font-weight: bold;
    font-family: 'Courier New', Courier, monospace;
    line-height: 1.2em;
    transform-origin: 0 0;
    rotate: 33deg;
    position: absolute;
    top: 50px;
    left: 70px;
  }
  #example18 textarea {
    width: 100%;
    box-sizing: border-box;
  }
</style>