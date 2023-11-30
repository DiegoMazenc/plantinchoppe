<script >

import NavBar from './components/NavBar.vue';
import Aside from './components/Aside.vue';
import PlantsCard from './components/PlantsCard.vue';

export default {
methods:{
  
}

}


</script>

<template>
  <nav>
 <NavBar/>
</nav>
<main class="main">
  <Aside class="aside"/>
  <PlantsCard @tri-alphabetique="" class="cards"/>
</main>
</template>

<style scoped>


.aside{
  width: 25%;
  height: 100vh;
  position: fixed;
  background-color: brown;
}
.main{
  display: flex;
}


</style>
