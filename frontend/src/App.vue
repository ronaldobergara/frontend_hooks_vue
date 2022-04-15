<template>
  <h1>{{ message }}!</h1>
  <h2>{{ count }}</h2>

  <button @click="count++" id="Increment">Incrementar</button>
  <button @click="destroyComponent">Desmontar</button>
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
  beforeUnmount() {
    console.log('Salvar a contagem no db')
  },
  unmounted() {
    alert('obrigado por utilizar o contador')
  },
  methods: {
    destroyComponent() {
      this.$.appContext.app.unmount(this.$el)
    }
  }
})
</script>

<style>
#Increment {
  margin-right: 5px;
}
</style>
