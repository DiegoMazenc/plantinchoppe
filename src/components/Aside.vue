<script>
export default {
  name: "Aside",
  methods: {
    trierAlphabetiquement() {
      this.$emit("tri-alphabetique");
      
    },
  },
};
</script>

<template>
    <div class="aside">
      <h3>Trier par</h3>
      <button @click="trierAlphabetiquement">Alphabétique</button>
      <div>Prix</div>
      <hr />
      <div>type</div>
      <div>difficulté</div>
      <div>couleur</div>
    </div>
  </template>

<style>

</style>