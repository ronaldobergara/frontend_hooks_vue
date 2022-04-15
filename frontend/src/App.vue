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
  beforeCreate() {
    console.log('Antes da Criação')
    console.log(this.message)
  },
  created() {
    console.log('Depois da Criação')
    console.log(this.message)
  }
})
</script>

<style></style>
