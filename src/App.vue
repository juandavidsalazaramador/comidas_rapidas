<template>
  <q-layout view="hHh lpR fFf">

    <q-header elevated class="bg-primary text-white">
      <q-toolbar>
        <q-btn
          dense
          flat
          round
          icon="menu"
          @click="toggleLeftDrawer"
        />

        <q-toolbar-title>
          🍔 Menú Digital
        </q-toolbar-title>
      </q-toolbar>
    </q-header>

    <q-drawer
      v-model="leftDrawerOpen"
      side="left"
      bordered
    >
      <q-list padding>

        <q-item clickable v-close-popup to="/">
          <q-item-section>Inicio</q-item-section>
        </q-item>

        <q-item clickable v-close-popup to="/hamburguesas">
          <q-item-section>🍔 Hamburguesas</q-item-section>
        </q-item>

        <q-item clickable v-close-popup to="/perros">
          <q-item-section>🌭 Perros</q-item-section>
        </q-item>

        <q-item clickable v-close-popup to="/pizzas">
          <q-item-section>🍕 Pizzas</q-item-section>
        </q-item>

        <q-item clickable v-close-popup to="/bebidas">
          <q-item-section>🥤 Bebidas</q-item-section>
        </q-item>

        <q-item clickable v-close-popup to="/postres">
          <q-item-section>🍰 Postres</q-item-section>
        </q-item>

        <q-item clickable v-close-popup to="/promociones">
          <q-item-section>🔥 Promociones</q-item-section>
        </q-item>

        <q-item clickable v-close-popup to="/nosotros">
          <q-item-section>👨‍🍳 Nosotros</q-item-section>
        </q-item>

      </q-list>
    </q-drawer>

    <q-page-container>
      <router-view />
    </q-page-container>

    <q-footer elevated class="bg-grey-8 text-white">
      <q-toolbar>
        <q-toolbar-title class="text-center">
          Menú Digital · Comidas Rápidas
        </q-toolbar-title>
      </q-toolbar>
    </q-footer>

  </q-layout>
</template>

<script setup>
import { ref } from 'vue'

const leftDrawerOpen = ref(false)

function toggleLeftDrawer () {
  leftDrawerOpen.value = !leftDrawerOpen.value
}
</script>