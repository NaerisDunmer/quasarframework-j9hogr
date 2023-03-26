<template>
  <q-page class="column flex-center">
    Guten Tag!
    <br>
    Bitte melden Sie sich an:
    <br>
    <br>
    <q-input v-model="name" color="#3f474e" label="Benutzername" filled>
    </q-input>
    <br>
    <q-input v-model="passwort" color="#3f474e" label="Passwort" filled>
    </q-input>

  </q-page>
</template>

<script setup>
import { ref } from 'vue';

const count = ref(0);

const min = -5;
const max = 5;
</script>