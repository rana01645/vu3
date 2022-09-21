<template>
  <div class="hello">


    <input v-model="form.name" type="text">
    <input v-model="form.email" type="text">
    <input v-model="form.password" type="password">

  </div>
</template>

<script setup>
import {inject} from "vue";

const form = inject('form')

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
