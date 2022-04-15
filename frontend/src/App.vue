<template>
  <h1>{{ message }}!</h1>
</template>

<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
  data() {
    return {
      message: 'Hello Kaori'
    }
  },
  beforeMount() {
    console.log('Antes da Montagem')
    console.log(this.message)
    console.log(this.$el) // Acessa o primeiro elemento raiz e retorna null porque não tem acesso
  },
  mounted() {
    console.log('Depois da Montagem')
    console.log(this.message)
    console.log(this.$el) // Acessa o primeiro elemento raiz
    this.$el.style.background = 'red' // Alteração na DOM
  }
})
</script>

<style></style>
