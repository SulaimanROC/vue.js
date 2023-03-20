<template>
  <div class="vac">
    <h1>VacationPicker</h1>
    <p>Aantal = {{count}}</p>
    <button class="btn btn-success" v-on:click="count++" >Plus</button>
    <button class="btn btn-danger" @click="count--"> Min </button>

    <h2>Lijst</h2>
    <ul class="list-group">
        <li class="list-group-item" v-for="(number, index) in numberList" v-bind:key="index"> 
            {{number}}
        </li>
    </ul>

  </div>
</template>

<script>
export default {
  name: 'VacationPicker',
  data(){
    return{
        count:0,
        numberList: [1,2,3,4]
    }
  }
        
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
