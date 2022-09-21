<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <h1>Example 1: Use object as V-model</h1>
  <form>
    {{state.form}}
    <ObjecVModel v-model="state.form"/>
    <button type="submit">Submit</button>
  </form>

  <h1>Example 1: Use provide and inject in form</h1>
  <form>
    <ProvidAndInject/>
    <button type="submit">Submit</button>
  </form>
</template>

<script setup>
import {provide, reactive} from "vue";
import ObjecVModel from "@/components/ObjecVModel.vue";
import ProvidAndInject from "@/components/ProvidAndInject.vue";

const state = reactive({
  form: {
    name: 'test',
    email: '',
    password: ''
  }
})

provide('form', state.form)
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
