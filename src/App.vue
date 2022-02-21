<template>
  <h2>Prix total HT : {{ totalPrixHT }}€</h2>
  <h2>Prix total TTC : {{ totalPrixTTC }}€</h2>
</template>

<script setup lang="ts">
import { computed, reactive } from 'vue';

const produit = reactive({
  quantite: 3,
  prix: 10,
  nom: 'livre',
});

const totalPrixHT = computed(() => produit.quantite * produit.prix);
const totalPrixTTC = computed(() => produit.quantite * produit.prix * 1.2);
</script>

<style></style>
