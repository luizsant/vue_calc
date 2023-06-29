<template>
  <div class="container">
    <h1>Calculadora Aritmética</h1>
    <Calculadora />
  </div>
</template>

<script>
import Calculadora from "./components/Calculadora.vue";

export default {
  components: {
    Calculadora
  }
};
</script>

<style scoped>
.container {
  max-width: 400px;
  margin: 0 auto;
  text-align: center;
  padding: 20px;
}
</style>
