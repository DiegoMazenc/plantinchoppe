<script setup>
import NavBar from './components/NavBar.vue';
import Footer from './components/Footer.vue';
import PlantsCard from './components/PlantsCard.vue';
</script>

<template>
 <NavBar/>
 <PlantsCard/>

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
