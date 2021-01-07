<template>
  <h1>First Vue app modal</h1>
  <div class="row">
    <input type="text" ref="name" />
    <button class="btn-primary" @click="clickHandle()">Click</button>
    <Modal :header="header" :text="text" :theme="sale" />
  </div>
</template>

<script>
import Modal from "./components/Modal";
export default {
  name: "App",
  data() {
    return {
      header: "Signup for Giveaway!",
      text: 'Grab your swag for half price',
      sale: 'sale' 
    };
  },
  components: { Modal },
  methods: {
    clickHandle() {
      this.$refs.name.classList.add("active");
      this.$refs.name.focus();
    },
  },
};
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
