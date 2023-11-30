<script>
import stockplantes from './data/stockplantes.json';

export default {
  name: 'PlantsCard',
  props: {
    triAlphabetique: Boolean,
    triPrix : Boolean, 
  },
  data() {
    return {
      plantesListe: stockplantes,
    };
  },
  watch: {
    triAlphabetique() {
      this.trierListe();
    },
    triPrix() {
      this.trierPrix();
    },
  },
  methods: {
    trierListe() {
      if (this.triAlphabetique) {
     
        this.plantesListe.sort((a, b) => (a.name > b.name ? 1 : -1));
      }
    },
    trierPrix() {
      if (this.triPrix) {
     
        this.plantesListe.sort((a, b) => (a.price > b.price ? 1 : -1));
      }
    },
  },
  // mounted() {
  //   this.trierListe();
  // },
};
</script>

<template>
<div class="cardCard">
  <div v-for="(plante, index) in plantesListe" :key="index" class="card cardContain" >
    <img :src="plante.image" class="card-img-top imgCardSize" alt="..." />
    <div class="card-body">
      <h5 class="card-title">{{ plante.name }}</h5>
      <p class="card-text">Prix : {{plante.price}}€</p>
      <p class="card-text">Difficulté d'entretien : {{plante.entretien}}</p>
      <p class="card-text">Taille : {{plante.taille}}</p>
      <p class="card-text">Luminosité : {{plante.luminosité}}</p>
      <p class="card-text">couleur : {{plante.couleur}}</p>
      <a href="#" class="btn btn-primary">Go somewhere</a>
    </div>
  </div>
</div>
</template>

<style scoped>
.cardCard{
  width: 75%;
  margin-left: 25%;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-evenly;

}

.cardContain{
  width: 350px;
  margin: 10px;
}

.imgCardSize{
height: 200px;
}
</style>
