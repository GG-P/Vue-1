<template>
  <div>
    <input v-model="name" placeholder="Write search name" />
    <br />
    <div>
      <select v-model="category">
        <option> value="Book" Books</option>
        <option> value="Magazine" Magazines</option>
        <option> value="Newspaper" Newspapers</option>
        <option> value="Other" Others</option>
        <option> value="All" All</option>      
        </select>
    </div>

     <div :key="item.name">
      <p>Name: {{ item.name }}</p>
      <p>Description: {{ item.description }}</p>
    </div>

export default {
    name:""
}

data () {
    return{
        code: "?"
        name: "test"
        description: "blabla"
        category: "Book"
    }    
}
computed: {
    filteredList(){
        return this.list.filter(
        item => item.name === this.message || item.description == this.message
    }
}
