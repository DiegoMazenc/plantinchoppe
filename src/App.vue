<script setup>
import NavBar from './components/NavBar.vue';
import Footer from './components/Footer.vue';
</script>

<template>
 <NavBar/>

 <Footer class="footer-container"/>

</template>

<style scoped>
body{
  background-color: rgb(36, 36, 36);
}

.footer-container{
    background-color: green;
}

</style>
