<script>

import stockplantes from '../data/stockplantes.json'

export default {
  name: 'PlantsCard',

  //The imported module should be store as an object so a new proprety as to be set
  data() {
    return {plantesListe: stockplantes}; 
  },
  mounted() {
    console.log(this.plantesListe); 
  },
}

</script>

<template>

  <div v-for="(plante, index) in plantesListe" :key="index" class="card" style="width: 18rem">
    <img src="..." class="card-img-top" alt="..." />
    <div class="card-body">
      <h5 class="card-title">{{ plante.name }}</h5>
      <p class="card-text">{{plante.price}}</p>
      <a href="#" class="btn btn-primary">Go somewhere</a>
    </div>
  </div>

</template>

<style scoped></style>
