<template>
  <div>
    <h1>Example: Count Input Events</h1>

    <div id="example12">
      <input type="text" v-on:input="inpCount++" placeholder="Start writing..">
      <p>{{ 'Input events occured: '+inpCount }}</p>
    </div>
  </div>
</template>
<script>
export default {
  name: 'T12voninput',
  components: {},
  data(){
    return {
      inpCount: 0
    }
  }
}
</script>
<style lang="css">
  #example12 {
    border: dashed black 1px;
    width: 200px;
    padding: 20px;
  }
</style>