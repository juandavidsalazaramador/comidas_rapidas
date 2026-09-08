<template>
  <q-page class="q-pa-md q-pa-lg-lg">
    <CategoryBanner
      image="https://loremflickr.com/1200/400/dessert/all?lock=501"
      title="🍰 Postres"
      description="El final dulce perfecto: preparaciones caseras horneadas todos los días en nuestra cocina."
    />

    <div class="row q-col-gutter-lg">
      <div
        v-for="product in productos"
        :key="product.id"
        class="col-12 col-sm-6 col-md-3"
      >
        <ProductCard :product="product" />
      </div>
    </div>

    <ChefRecommendation :product="recomendacion" />
  </q-page>
</template>

<script setup>
import CategoryBanner from '../components/CategoryBanner.vue'
import ProductCard from '../components/ProductCard.vue'
import ChefRecommendation from '../components/ChefRecommendation.vue'

const productos = [
  {
    id: 1,
    name: 'Brownie con Helado',
    description: 'Brownie tibio de chocolate con bola de helado de vainilla y salsa de chocolate.',
    price: '$12.500',
    image: 'https://loremflickr.com/500/400/brownie,icecream/all?lock=502',
    tag: 'Más pedido'
  },
  {
    id: 2,
    name: 'Cheesecake de Maracuyá',
    description: 'Base de galleta, queso crema y cobertura de maracuyá natural.',
    price: '$13.500',
    image: 'https://loremflickr.com/500/400/cheesecake/all?lock=503',
    tag: 'Nuevo'
  },
  {
    id: 3,
    name: 'Copa de Frutas',
    description: 'Mezcla de frutas frescas de temporada con miel y granola.',
    price: '$9.900',
    image: 'https://loremflickr.com/500/400/fruit,dessert/all?lock=504',
    tag: 'Vegetariano'
  },
  {
    id: 4,
    name: 'Waffle con Nutella',
    description: 'Waffle crocante bañado en Nutella, banano y almendras tostadas.',
    price: '$14.900',
    image: 'https://loremflickr.com/500/400/waffle,nutella/all?lock=505'
  }
]

const recomendacion = {
  name: 'Volcán de Chocolate Caliente',
  description: 'Bizcocho de chocolate horneado con centro líquido, acompañado de helado de vainilla y frutos rojos.',
  price: '$15.900',
  image: 'https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQugueeSHGyeK8GUJnT2H4OBGQZVDayoIAgGJYXWTlNsQ&s=10'
}
</script>
