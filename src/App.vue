<template>
  <h1>{{ title }}</h1>
  <teleport to="#modals" v-if="showModal">
    <!-- <Modal :header="header" :text="text" :theme="sale" @close="toggleModal" /> -->
    <Modal theme="sale" @close="toggleModal" >
      <template v-slot:links>
        <a href="">sign up now</a>
        <a href="">more info</a>
      </template>
      <h1>Sign up for Giveway!</h1>
      <p>Grap your ninja swag for half price!</p>
    </Modal>
  </teleport>

  <teleport to="#modals" v-if="showModalTwo">
    <!-- <Modal :header="header" :text="text" :theme="sale" @close="toggleModal" /> -->
    <Modal theme="sale" @close="toggleModalTwo" >
      
      <h1>Sign up to newsletter !</h1>
      <p>For update and promote codes!</p>
    </Modal>
  </teleport>
  <button @click="toggleModal()">open modal</button>
  <button @click="toggleModalTwo()">open modal two</button>
</template>

<script>

import Modal from './components/Modal.vue'
export default {
  name: 'App',
  components: { Modal },
  data(){
    return {
      title: 'My first Vue App :)',
      header: 'Sign up for Giveway!',
      text : 'Grap your ninja swag for half price!',
      showModal: false,
      showModalTwo: false
    }
  },
  methods: {
    toggleModal() {
      this.showModal = !this.showModal
    },
    toggleModalTwo() {
      this.showModalTwo = !this.showModalTwo
    }
  }
}
</script>

<style>
#app, .modals {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
