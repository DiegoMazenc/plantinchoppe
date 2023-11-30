<script setup>
import HelloWorld from './components/HelloWorld.vue'
import TheWelcome from './components/TheWelcome.vue'
import NavBar from './components/NavBar.vue'
import Aside from './components/Aside.vue'


</script>

<template>
 <NavBar/>
 <main>
  <Aside/>
 </main>
 
</template>

<style scoped>
main{
  display: flex;
}


</style>
