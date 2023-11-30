<script>

import NavBar from './components/navbar.vue';
import Aside from './components/Aside.vue';
import PlantsCard from './components/PlantsCard.vue';

export default {
  components: {
    NavBar,
    Aside,
    PlantsCard,
  },
  data() {
    return {
      triAlphabetique: false,
      triPrix: false,
      triTaille: false,
    };
  },
  methods: {
    handleTriAlphabetique() {
      this.triPrix = false; 
      this.triAlphabetique = true;
    },

    handleTriPrix() {
      this.triAlphabetique = false;
      this.triPrix = true;
    },

    handleTriTaille(){
      this.triTaille = true
    }
  },
};
</script>


<template>
  <div>
    <NavBar/>
    <main class="main">
      <Aside @tri-alphabetique="handleTriAlphabetique" @tri-prix="handleTriPrix" @Grande="handleTriTaille" class="aside" />
      <PlantsCard :triAlphabetique="triAlphabetique" :triPrix="triPrix" :triTaille="triTaille" class="cards" />
    </main>
  </div>
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
