<template>
    <h2>Hola Mundo</h2>
    <p>{{ message }}</p>
    <label id="message">Mensaje</label><br/>
    <input id="message" v-model="message">

</template>

<script>

import { ref } from "vue"

export default {
  name: 'HomeWorld',
   setup() {
     const message = ref("Hola a todos")
    return {message}
  }
}
</script>