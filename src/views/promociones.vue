<template>
  <q-page class="q-pa-md q-pa-lg-lg">
    <CategoryBanner
      image="https://loremflickr.com/1200/400/fastfood,combo/all?lock=601"
      title="🔥 Promociones"
      description="Combos especiales pensados para compartir y ahorrar. ¡Válidas todos los días hasta agotar existencias!"
    />

    <div class="row q-col-gutter-lg">
      <div
        v-for="promo in promociones"
        :key="promo.id"
        class="col-12 col-sm-6 col-md-4"
      >
        <q-card class="product-card" flat bordered>
          <q-img :src="promo.image" :ratio="4/3">
            <q-badge color="negative" floating class="text-weight-bold q-pa-sm" style="font-size: 12px; border-radius: 8px;">
              {{ promo.descuento }}
            </q-badge>
          </q-img>
          <q-card-section>
            <div class="text-h6 font-title text-weight-bold">{{ promo.name }}</div>
            <div class="text-body2 text-grey-8 q-mt-xs">{{ promo.description }}</div>
          </q-card-section>
          <q-separator inset />
          <q-card-section class="row items-center justify-between">
            <div>
              <span class="text-caption text-grey text-strike q-mr-sm">{{ promo.precioAntes }}</span>
              <span class="text-h6 text-weight-bold" style="color: #E63946;">{{ promo.precioAhora }}</span>
            </div>
            <q-btn round color="primary" icon="local_fire_department" size="sm" />
          </q-card-section>
        </q-card>
      </div>
    </div>
  </q-page>
</template>

<script setup>
import CategoryBanner from '../components/CategoryBanner.vue'

const promociones = [
  {
    id: 1,
    name: 'Combo Pareja',
    description: '2 hamburguesas clásicas + papas grandes para compartir + 2 bebidas.',
    precioAntes: '$52.000',
    precioAhora: '$42.900',
    descuento: '-18%',
    image: 'https://www.shutterstock.com/image-photo/couple-eating-fresh-burger-sitting-260nw-2467344755.jpg'
  },
  {
    id: 2,
    name: 'Noche de Pizza',
    description: 'Pizza mediana a elección + gaseosa 1.5L + porción de pan de ajo.',
    precioAntes: '$41.000',
    precioAhora: '$33.500',
    descuento: '-18%',
    image: 'https://thumbs.dreamstime.com/b/pizza-de-queso-en-el-disco-m%C3%A1s-cercano-1947409.jpg'
  },
  {
    id: 3,
    name: 'Combo Familiar',
    description: '4 perros calientes + papas hilo grandes + 4 bebidas + 1 postre para compartir.',
    precioAntes: '$78.000',
    precioAhora: '$64.900',
    descuento: '-17%',
    image: 'https://previews.123rf.com/images/sonyakamoz/sonyakamoz2102/sonyakamoz210200022/163950083-lockdown-family-fast-food-dinner-from-delivery-service-flat-lay-of-friends-group-eating-burgers.jpg'
  }
]
</script>
