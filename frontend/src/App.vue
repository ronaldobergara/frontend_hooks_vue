<template>
  <h1>{{ message }}!</h1>
  <h2>{{ count }}</h2>

  <button @click="count++" id="Increment">Incrementar</button>
  <button @click="count--">Decrementar</button>
</template>

<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
  data() {
    return {
      message: 'Hello Kaori',
      count: 0
    }
  },
  beforeUpdate() {
    console.log('Antes da Alteração')

    if (this.count == 2) {
      this.count = 5
    }

    console.log(this.count)
  },
  updated() {
    console.log('Depois da Alteração')
    console.log(this.count)
  }
})
</script>

<style>
#Increment {
  margin-right: 5px;
}
</style>
