<template>
  <q-page class="q-pa-md q-pa-lg-lg">
    <div
      class="category-banner q-mb-xl"
      style="min-height: 340px; background-image: url('https://loremflickr.com/1400/500/fastfood,restaurant/all?lock=1'); background-size: cover; background-position: center;"
    >
      <div class="banner-overlay"></div>
      <div class="banner-content">
        <div class="text-h3 text-h4-sm text-weight-bold font-title">El mejor sabor en comidas rápidas</div>
        <p class="text-subtitle1 q-mt-sm" style="max-width: 620px;">
          Hamburguesas, perros calientes, pizzas, bebidas y postres preparados al momento,
          con ingredientes frescos y mucho sabor.
        </p>
        <q-btn to="/promociones" color="secondary" text-color="dark" unelevated rounded size="lg" class="q-mt-md">
          Ver promociones 🔥
        </q-btn>
      </div>
    </div>

    <div class="text-h5 font-title text-weight-bold q-mb-md text-center">Explora nuestro menú</div>

    <div class="row q-col-gutter-md">
      <div v-for="cat in categorias" :key="cat.to" class="col-6 col-sm-4 col-md-3">
        <router-link :to="cat.to" custom v-slot="{ navigate }">
          <q-card @click="navigate" clickable v-ripple class="product-card text-center">
            <q-img :src="cat.image" :ratio="1" />
            <q-card-section>
              <div class="text-subtitle1 text-weight-bold font-title">{{ cat.name }}</div>
            </q-card-section>
          </q-card>
        </router-link>
      </div>
    </div>
  </q-page>
</template>

<script setup>
const categorias = [
  { name: '🍔 Hamburguesas', to: '/hamburguesas', image: 'https://images.unsplash.com/photo-1568901346375-23c9450c58cd?auto=format&fit=crop&w=600&q=80' },
  { name: '🌭 Perros', to: '/perros', image: 'https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTd0adP9B4T3c9IVH_en-O3rttLepzGP3bKjQgs44SOTw&s=10' },
  { name: '🍕 Pizzas', to: '/pizzas', image: 'https://images.unsplash.com/photo-1513104890138-7c749659a591?auto=format&fit=crop&w=600&q=80' },
  { name: '🥤 Bebidas', to: '/bebidas', image: 'https://images.unsplash.com/photo-1544145945-f90425340c7e?auto=format&fit=crop&w=600&q=80' },
  { name: '🍰 Postres', to: '/postres', image: 'https://images.unsplash.com/photo-1551024601-bec78aea704b?auto=format&fit=crop&w=600&q=80' },
  { name: '🔥 Promociones', to: '/promociones', image: 'https://images.unsplash.com/photo-1555939594-58d7cb561ad1?auto=format&fit=crop&w=600&q=80' },
  { name: '👨‍🍳 Nosotros', to: '/nosotros', image: 'https://images.unsplash.com/photo-1556910103-1c02745aae4d?auto=format&fit=crop&w=600&q=80' }
]
</script>
