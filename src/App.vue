<template>
<div>
  <img alt="Vue logo" src="./assets/logo.png" />
  <HelloWorld msg="Hello Vue 3.0 + Vite" />
  <TestPage></TestPage>
</div>
  
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import TestPage from "./components/TestPage.vue"




export default {
  name: 'App',
  components: {
    HelloWorld,
    TestPage,
  },
  
}
</script>
