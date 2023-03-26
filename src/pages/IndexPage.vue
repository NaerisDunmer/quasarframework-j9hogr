<template>
  <q-page class="column flex-center">
    Guten Tag!
    Bitte melden Sie sich an:
    <q-input v-model="name"></q-input>
    <q-input v-model="passwort"></q-input>
  </q-page>
</template>

<script setup>
import { ref } from 'vue';

const count = ref(0);

const min = -5;
const max = 5;
</script>
