<template>
   <div class="header">
      <img alt="Logo" src="./assets/logo.jpg">
      <div class="menus">
          <div @click="scrollToBottom('products')">Müük</div>
          <div @click="scrollToBottom('contact')">Kontakt</div>
      </div>
  </div>

  <div ref="products"></div>
  <ProductsView />

  <div ref="contact"></div>
  <ContactView />
</template>

<script>
import ProductsView from './components/ProductsView.vue'
import ContactView from './components/ContactView.vue'

export default {
  name: 'App',
  components: {
    ProductsView, ContactView
  },
  methods: {
        scrollToBottom(element) {
            this.$refs[element]?.scrollIntoView({ behavior: 'smooth' });
        },
  },
}
</script>

<style>
img {
    width: 200px;
}

.header {
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 30px;
    position: fixed;
    top: 0;
    width: 100%;
    background: white;
    height: 200px;
}

.menus {
    display: flex;
    gap: 20px
}
</style>
