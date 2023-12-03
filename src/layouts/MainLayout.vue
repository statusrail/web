<template>
  <q-toolbar class="bg-white text-blue q-my-md">
    <q-btn-dropdown stretch flat no-caps label="Status Rail">
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
    <q-btn stretch flat no-caps label="GitHub" />
  </q-toolbar>
  <q-separator blue inset />
  <q-img
    src="../assets/bg.png"
    spinner-color="white"
    img-class="background-image"
    class="rounded-borders"
  />
</template>

<script lang="ts">
import { defineComponent, ref } from 'vue';

export default defineComponent({
  name: 'MainLayout',

  setup () {
    return {
      tab: ref('images')
    }
  }
});
</script>
