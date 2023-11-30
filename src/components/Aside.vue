<script>
export default {
  name: "Aside",
  methods: {
    trierAlphabetiquement() {
      this.$emit("tri-alphabetique")
},

trierParPrix () {
  this.$emit("tri-prix")
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
      <div>type</div>
      <div>difficulté</div>
      <div>couleur</div>
    </div>
  </template>

<style>

</style>