<template>
  <q-layout view="lHh Lpr lFf">
    <q-toolbar class="bg-white q-my-auto text-blue ">
      <q-btn-dropdown stretch flat no-caps label="statusrail">
        <q-list>
          <q-item-label header>Projects</q-item-label>
          <q-item v-for="n in 3" :key="`x.${n}`" clickable v-close-popup tabindex="0">
            <q-item-section>
              <q-item-label>Project</q-item-label>
              <q-item-label caption>Description</q-item-label>
              <q-separator inset spaced />
            </q-item-section>
          </q-item>
        </q-list>
      </q-btn-dropdown>
      <q-space />
      <q-btn flat no-caps stretch @click="goToGitHub">
        <q-icon class="text-dark" size="md">
          <img src="../assets/github.svg"  alt="GitHub"/>
        </q-icon>
      </q-btn>
    </q-toolbar>
    <q-separator blue inset />
    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script lang="ts">
import { defineComponent, ref } from 'vue';

export default defineComponent({
  name: 'MainLayout',

  setup () {
    return {
      tab: ref('images')
    }
  },

  methods: {
    goToGitHub() {
      window.open('https://github.com/statusrail');
    },
  }
});
</script>
