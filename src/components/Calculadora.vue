<template>
  <div class="calculadora">
    <input type="number" v-model="numero1" @input="calcularResultado" />
    <select v-model="operacao" @change="calcularResultado">
      <option value="+">+</option>
      <option value="-">-</option>
      <option value="*">*</option>
      <option value="/">/</option>
    </select>
    <input type="number" v-model="numero2" @input="calcularResultado" />
    <h2>Resultado: {{ resultado }}</h2>
  </div>
</template>

<script>
export default {
  data() {
    return {
      numero1: 0,
      numero2: 0,
      operacao: "+",
      resultado: 0
    };
  },
  methods: {
    calcularResultado() {
      const num1 = parseFloat(this.numero1);
      const num2 = parseFloat(this.numero2);

      switch (this.operacao) {
        case "+":
          this.resultado = num1 + num2;
          break;
        case "-":
          this.resultado = num1 - num2;
          break;
        case "*":
          this.resultado = num1 * num2;
          break;
        case "/":
          this.resultado = num1 / num2;
          break;
        default:
          this.resultado = 0;
      }
    }
  }
};
</script>

<style scoped>
.calculadora {
  display: flex;
  flex-direction: column;
  align-items: center;
  margin-top: 50px;
}

input,
select {
  margin-bottom: 10px;
  padding: 5px;
}
</style>
