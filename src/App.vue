<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <Reactivity/>
  <ConditionalRendering class="gap"/>
  <ClassStyleBinding class="gap"/>
  <ListRendering class="gap"/>
  <EventFormBinding class="gap"/>
</template>

<script>
import Reactivity from './components/Reactivity.vue'
import ConditionalRendering from './components/ConditionalRendering.vue'
import ClassStyleBinding from './components/ClassStyleBinding.vue'
import ListRendering from './components/ListRendering.vue'
import EventFormBinding from './components/EventFormBinding.vue'

export default {
  name: 'App',
  components: {
    Reactivity,
    ConditionalRendering,
    ClassStyleBinding,
    ListRendering,
    EventFormBinding
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin: 60px 0;
}
.gap {
    margin-top: 24px;
}
</style>
