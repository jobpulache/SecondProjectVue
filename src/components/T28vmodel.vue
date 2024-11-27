<template>
  <div>
    <h1>Example: Important Checkbox</h1>
    <p>This 'important' checkbox is a dynamic form feature that will be added to a shoppinglist form later, but we isolate it here first to easier see how it works.</p>
    <div id="example28">
      <form>
        <p>
          Important item?
          <label>
            <input type="checkbox" v-model="important"> 
            {{ important }}
          </label>
        </p>
      </form>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      important: false
    }
  }
}
</script>
<style lang="css">
  #example28 > form {
    border: dashed black 1px;
    display: inline-block;
    padding: 10px;
  }
  #example28 > label {
    padding: 5px;
  }
  #example28 > label:hover {
    cursor: pointer;
    background-color: lightgray;
    border-radius: 5px;
  }
</style>