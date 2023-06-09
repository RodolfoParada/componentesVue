<template>
    <h1>Reactive Counter</h1>
    <h3>
        {{counter }}
    </h3>
    <h3>{{  couterComputed }}</h3>
     <button @click="increment">Incrementar</button>
        <button @click="decrement">Decrementar</button>

    </template>

<script>
import {reactive, computed, toRefs, toRef} from "vue"

export default {
    name: "ReactiveCounter",
    setup() {
        const data = reactive({
            counter: 0,
            counterComputed: computed(() => {
                return `El valor de counter es ${data.counter}`
            })
        })
        const increment = () => {
            data.counter++
        }
        const decrement = () => {
            data.counter--
        }
         return { ...toRefs(data), increment, decrement}  
    }
}
  

</script>



<script />