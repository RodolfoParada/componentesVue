<template>

  <hr/>
  <Emit @onFire="eventEmittedFromChild"/>
  <hr/>
    <profile-with-props name="Cursosdesarrolloweb" :age="39"/>
  <hr/>
     <simple-fetch />
  <hr/>

   <hr/> 
   <todo-list/>

  <hr>
  <counterComposition/>
  <hr/>
   <watchCounter/>
  <hr/>
  <reactive-counter/>
  <hr/>
  <simple-counter />
  <hr/>
  <hola-mundo/>
</template>

<script>
import holaMundo from '../components/00HelloWorl.vue'
import SimpleCounter from "@/components/01SImpleCounte.vue"
import ReactiveCounter from "@/components/02ReactiveCounter.vue"
import watchCounter from "@/components/03WatchCounter.vue"
import counterComposition from "@/components/04SimpleCounterComposition.vue"
import TodoList from "@/components/05TodoList.vue"
import simpleFetch from "@/components/06SimpleFetch.vue"
import profileWithProps from "@/components/07ProfileWithProps.vue"
import Emit from "@/components/08EmitEvents.vue"

export default {
  name: 'HomeView',
  components: {
    holaMundo,
    SimpleCounter,
    ReactiveCounter,
    watchCounter,
    counterComposition,
    TodoList,
    simpleFetch,
    profileWithProps,
    Emit,
    
  },
  setup() {
    
    
    // const message = "Mensaje desde el componente Helloworld"
    // return { message }
    
    const eventEmittedFromChild = (message) => {
      console.log(message)
    }
    return { eventEmittedFromChild }
    
  }
}
</script>

