<template>
  <NavBar />
  <ProductsView />
  <ContactView />
</template>

<script>
import NavBar from './components/NavBar.vue'
import ProductsView from './components/ProductsView.vue'
import ContactView from './components/ContactView.vue'
import { ref } from 'vue'

const bottomEl = ref(null)

export default {
  name: 'App',
  props: {
    bottomEl
  },
  components: {
    NavBar, ProductsView, ContactView
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
</style>
