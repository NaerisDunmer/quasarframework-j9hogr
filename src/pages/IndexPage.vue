<template>
  <q-page class="column flex-center">
    Guten Tag!
    Bitte melden Sie sich an:
    <br>
    <q-input v-model="name" color="blue" label="Benutzername" filled>Benutzername:</q-input>
    <br>
    <q-input v-model="passwort" color="blue" label="Passwort" filled></q-input>
  </q-page>
</template>

<script setup>
import { ref } from 'vue';

const count = ref(0);

const min = -5;
const max = 5;
</script>
