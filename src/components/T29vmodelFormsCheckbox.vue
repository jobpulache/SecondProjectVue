<template>
  <div>
    <h1>Example: Shopping List With Important Items</h1>
    <p>In this version of our shopping list the user can define if an item is important. The checkbox is more dynamic because the 'true' or 'false' text changes to show the status when the user checks it.</p>
    <div id="example29">
      <form v-on:submit.prevent="addItem">
        <p>
          What do you need? <br>
          <input type="text" required placeholder="item name.." v-model="itemName">
        </p>
        <p>
          How many? <br>
          <input type="number" placeholder="number of items.." v-model="itemNumber">
        </p>
        <p>
          Important?
          <label>
            <input type="checkbox" v-model="itemImportant">
            {{ itemImportant }}
          </label>
        </p>
        <button type="submit">Add item</button>
      </form>
      <br>
      <hr>

      <div>
        <p><strong>Shopping list:</strong></p>
        <ul>
          <li v-for="item in shoppingList" v-bind:class="{ impClass: item.important }">{{ item.name }}, {{ item.number}}</li>
        </ul>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      itemName: null,
      itemNumber: null,
      itemImportant: false,
      shoppingList: [
        { name: 'Tomatoes', number: 5, important: false }
      ]
    }
  },
  methods: {
    addItem(){
      let item = {
        name: this.itemName,
        number: this.itemNumber,
        important: this.itemImportant
      }
      this.shoppingList.push(item)
      this.itemName = null
      this.itemNumber = null  
      this.itemImportant = false
    }
  }
}
</script>
<style lang="css">
  #example29 {
    border: dashed black 1px;
    display: inline-block;
    padding: 0 20px;
  }
  #example29 label {
    padding: 5px;
  }
  #example29 label:hover {
    cursor: pointer;
    background-color: lightgray;
    border-radius: 5px;
  }
  #example29 > ul {
    list-style-type: none;
  }
  #example29 > li {
    border-radius: 5px;
    padding: 5px;
    margin: 2px;
    background-color: rgb(211, 254, 211);
  }
  .impClass {
    background-color: rgb(255, 202, 202);
    font-weight: bold;
  }
</style>