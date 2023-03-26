<template>
  <q-layout view="lHh Lpr lFf">
    <q-header class="bg-blue-8" elevated>
      <q-toolbar>
        <q-btn
          flat
          dense
          round
          icon="menu"
          aria-label="Menu"
          @click="toggleLeftDrawer"
        />

        <q-toolbar-title>Elektrisiert durch den Tag</q-toolbar-title>

        <div>Quasar v{{ $q.version }}</div>
      </q-toolbar>
    </q-header>

    <q-drawer v-model="leftDrawerOpen" show-if-above bordered>
      <q-list>
        <q-item-label header>Weitere Informationen</q-item-label>

        <EssentialLink
          v-for="link in essentialLinks"
          :key="link.title"
          v-bind="link"
        />
      </q-list>
    </q-drawer>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
import { defineComponent, ref } from 'vue';
import EssentialLink from 'components/EssentialLink.vue';

const linksList = [
  {
    title: 'Registrierung',
    caption: 'Neues Konto anlegen',
    icon: 'school',
    link: 'https://www.hochschule-ruhr-west.de/schnelleinstieg/suche/',
  },
  {
    title: 'Wer hilft bei Problemen?',
    caption: 'Support kontaktieren',
    icon: 'record_voice_over',
    link: 'https://www.hochschule-ruhr-west.de/schnelleinstieg/kontakt/',
  },
];

export default defineComponent({
  name: 'MainLayout',

  components: {
    EssentialLink,
  },

  setup() {
    const leftDrawerOpen = ref(false);

    return {
      essentialLinks: linksList,
      leftDrawerOpen,
      toggleLeftDrawer() {
        leftDrawerOpen.value = !leftDrawerOpen.value;
      },
    };
  },
});
</script>
