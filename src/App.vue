<template>
  <h1>{{title}}</h1>

  <div v-if="showModal">
    <Modal theme="sale" @close = "toggleModal">
      <h1>Sign up for the giveaway!</h1>
      <p>Grab your ninja swag for half the price</p>

      <template v-slot:links>
        <a href="#">Sign Up</a>
        <a href="#">More info</a>
      </template>
    </Modal>  
  </div>

  <div v-if="showModalTwo">
    <Modal theme="sale" @close = "toggleModalTwo">
      <h1>Another Modal</h1>
      <p>Conditions apply</p>
    </Modal>  
  </div>

  <button @click="toggleModal">Open modal</button>
  <button @click="toggleModalTwo">Open modal Two</button>
</template>


<script lang="ts">
import { defineComponent } from 'vue';
import Modal from './components/Modal.vue';

export default defineComponent({
  name: 'App',
  components: {Modal},
  data() {
    return {
      title: "Modal Project", 
      showModal: false,
      showModalTwo: false
    }
  },
  methods: {
    toggleModal () {
      this.showModal = !this.showModal;
    },
    toggleModalTwo () {
      this.showModalTwo = !this.showModalTwo;
    }
  }
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
