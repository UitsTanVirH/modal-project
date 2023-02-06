<template>
  <h1>{{title}}</h1>
  <Modal/>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import Modal from './components/Modal.vue';

export default defineComponent({
  name: 'App',
  components: {Modal},
  data() {
    return {
      title: "Welcome to vue"
    }
  },
});
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
