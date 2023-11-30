<script>
export default {
  name: "Aside",
  data() {
    return {
        uneClass: "hefhehfe"
    }
  },
  methods: {
    trierAlphabetiquement() {
      this.$emit("tri-alphabetique")
    },
    trierParPrix () {
        this.uneClass = "prout"
        this.$emit("tri-prix")
    },
    trierParTaille(event) {
        this.$emit("tri-taille", event.target.value);
    },

        // trierParEntretien(event) {
        //   this.$emit("tri-Entretien", event.target.value);
        // },
    },
};
</script>

<template>
    <div class="aside">
      <h3 class="hvhv" :class="uneClass">Trier par</h3>
      <button @click="trierAlphabetiquement">Alphabétique</button>
      <button @click="trierParPrix">Prix</button>
      <hr />
      <label for="taille">taille</label>
      <select  name="taille" id="taille" @change="trierParTaille">
        <option value="Sélectionner">Sélectionner</option>
        <option  value="Petite">Petite</option>
        <option value="Moyenne">Moyenne</option>
        <option value="Grande">Grande</option>
      </select><br/>
      <!-- <label for="Entretien">Entretien</label>
      <select  name="Entretien" id="Entretien" @change="trierParEntretien">
        <option value="Sélectionner">Sélectionner</option>
        <option  value="Faible">Faible</option>
        <option value="Moyenne">Moyenne</option>
        <option value="Élevée">Élevée</option>
      </select> -->
      <div>couleur</div>
    </div>
  </template>

<style>

</style>