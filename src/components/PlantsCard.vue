<script>

import plants from '../data/plants.js'

export default {
  name: 'PlantsCard',

  //The imported module should be store as an object so a new proprety as to be set
  data() {
    return plants; 
  }, 
  methods: {
    afficher() {
        console.log(this.plants); 
    }
  },
}

</script>

<template>
  <div class="card" style="width: 18rem">
    <img src="..." class="card-img-top" alt="..." />
    <div class="card-body">
      <h5 class="card-title">Yo</h5>
      <p class="card-text">
        Some quick example text to build on the card title and make up the bulk of the card's
        content.
      </p>
      <a href="#" class="btn btn-primary">Go somewhere</a>
      <a href="#" class="btn btn-primary" @click="afficher">Afficher dans la console</a>
    </div>
  </div>
</template>

<style scoped></style>
