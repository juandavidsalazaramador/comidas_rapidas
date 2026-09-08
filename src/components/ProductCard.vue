<template>
  <q-card class="product-card" flat bordered>
    <q-img :src="product.image" :ratio="4/3">
      <q-badge
        v-if="product.tag"
        :color="tagColor"
        floating
        class="text-weight-bold q-pa-sm"
        style="font-size: 12px; border-radius: 8px;"
      >
        {{ product.tag }}
      </q-badge>
    </q-img>

    <q-card-section>
      <div class="text-h6 font-title text-weight-bold">{{ product.name }}</div>
      <div class="text-body2 text-grey-8 q-mt-xs" style="min-height: 40px;">
        {{ product.description }}
      </div>
    </q-card-section>

    <q-separator inset />

    <q-card-section class="row items-center justify-between">
      <div class="text-h6 text-weight-bold" style="color: #E63946;">
        {{ product.price }}
      </div>
      <q-btn round color="primary" icon="add_shopping_cart" size="sm" />
    </q-card-section>
  </q-card>
</template>

<script setup>
import { computed } from 'vue'

const props = defineProps({
  product: { type: Object, required: true }
})

const tagColors = {
  'Nuevo': 'positive',
  'Más pedido': 'warning',
  'Picante': 'negative',
  'Vegetariano': 'accent'
}

const tagColor = computed(() => tagColors[props.product.tag] || 'primary')
</script>
