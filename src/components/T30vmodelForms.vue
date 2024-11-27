<template>
  <div>
    <h1>Example: Mark Found Items</h1>
    <p>In this version of our shopping list the user can mark found items by clicking them. Found items become visible in the found items list, and items not found yet appear in the top without strike through. All shopping list items are created in both lists with v-for, they are just made visible in one list or the other with v-show depending on the 'found' data property.</p>
    <p>If you find an item, but you click the wrong item in the list, you can just click it again to correct the mistake.</p>
    <div id="example30">
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
        <ul id="ulToFind">
          <li 
            v-for="item in shoppingList" 
            v-bind:class="{ impClass: item.important }"
            v-on:click="item.found=!item.found"
            v-show="!item.found">
              {{ item.name }}, {{ item.number}}
          </li>
        </ul>
        <ul id="ulFound">
          <li 
            v-for="item in shoppingList" 
            v-bind:class="{ impClass: item.important }"
            v-on:click="item.found=!item.found"
            v-show="item.found">
              {{ item.name }}, {{ item.number}}
          </li>
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
      important: false,
      shoppingList: [
        { name: 'Tomatoes', number: 5, important: false, found: false }
      ]
    }
  },
  methods: {
    addItem() {
      let item = {
        name: this.itemName,
        number: this.itemNumber,
        important: this.itemImportant,
        found: false
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
  #example30 {
    border: dashed black 1px;
    display: inline-block;
    padding: 0 20px;
  }
  #example30 label, #example30 li {
    padding: 5px;
    border-radius: 5px;
  }
  #example30 label:hover, #example30 li:hover {
    cursor: pointer;
    background-color: lightgray;
  }
  #example30 ul {
    list-style-type: none;
  }
  #example30 li {
    margin: 2px;
    background-color: rgb(211, 254, 211);
  }
  .impClass {
    background-color: rgb(255, 202, 202);
  }
  #ulFound li {
    text-decoration: line-through;
    background-color: rgb(230,230,230);
  }
</style>