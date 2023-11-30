<script>
export default {
  name: "Aside",
  methods: {
    trierAlphabetiquement() {
      this.$emit("tri-alphabetique")
},

trierParPrix () {
  this.$emit("tri-prix")
},

trierParTaille () {
  this.$emit("Grande")
}


  },
};
</script>

<template>
    <div class="aside">
      <h3>Trier par</h3>
      <button @click="trierAlphabetiquement">Alphabétique</button>
      <button @click="trierParPrix">Prix</button>
      <hr />
      <label for="taille">taille</label>
      <select  name="taille" id="taille" @change="trierParTaille">
        <option value="Sélectionner">Sélectionner</option>
        <option  value="Petite">Petite</option>
        <option value="Moyenne">Moyenne</option>
        <option value="Grande">Grande</option>
      </select>
      <div>difficulté</div>
      <div>couleur</div>
    </div>
  </template>

<style>

</style>