<script>
import NavBar from './components/NavBar.vue';
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
    };
  },
  methods: {
    handleTriAlphabetique() {
      this.triAlphabetique = true;
    },
  },
};
</script>


<template>
  <div>
    <NavBar />
    <main class="main">
      <Aside @tri-alphabetique="handleTriAlphabetique" class="aside" />
      <PlantsCard :triAlphabetique="triAlphabetique" class="cards" />
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
