<template>
  <h1>{{ title }}</h1>
  <p>Welcome!</p>
  <Modal v-if="showModal" theme="sales" @close="toggleModal">
    <h1>Ninja Giveaway</h1>
    <p>Grab your ninja swag for half the price!</p>
    <template v-slot:links>
      <a href="#">sign up now</a>
      <a href="#">more info</a>
    </template>
  </Modal>
  <Modal v-if="showModalTwo" theme="" @close="toggleModalTwo">
    <h1>Ninja Giveaway</h1>
    <p>Grab your ninja swag for half the price!</p>
    <template v-slot:links>
      <a href="#">sign up now</a>
      <a href="#">more info</a>
    </template>
  </Modal>
  <button @click.shift="toggleModal">Open modal (shift)</button>
  <button @click="toggleModalTwo">Open modal</button>
</template>

<script>
import Modal from './components/Modal'

export default {
  name: 'App',
  components: {
    Modal
  },
  data() {
    return {
      title: 'My First Vue App :)',
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
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
h1 {
  border-bottom: 1px solid #ddd;
  display: inline-block;
  padding: 25px;
}
</style>
