<template>
  <q-page class="q-pa-md q-pa-lg-lg">
    <CategoryBanner
      image="https://loremflickr.com/1200/400/beverages,drinks/all?lock=401"
      title="🥤 Bebidas"
      description="Refrescantes, naturales y heladas. La bebida perfecta para acompañar cualquiera de nuestros platos."
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
    name: 'Limonada de Coco',
    description: 'Limonada natural batida con crema de coco y hielo.',
    price: '$8.500',
    image: 'https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRABD-h-eSv0HaPM6oNLMpugP4_EGhQP6iTKduyzxlfIA&s=10',
    tag: 'Más pedido'
  },
  {
    id: 2,
    name: 'Malteada de Fresa',
    description: 'Helado de fresa, leche entera y crema chantilly.',
    price: '$11.500',
    image: 'https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSH-j-SLzJ1oPehqKj8LMWMS9r3A30pfSp3HPbp066rhw&s=10',
    tag: 'Nuevo'
  },
  {
    id: 3,
    name: 'Gaseosa 400ml',
    description: 'Disponible en Coca-Cola, Sprite o Fanta bien helada.',
    price: '$5.500',
    image: 'https://loremflickr.com/500/400/soda,cola/all?lock=404'
  },
  {
    id: 4,
    name: 'Jugo Verde Detox',
    description: 'Espinaca, manzana verde, apio y limón, 100% natural.',
    price: '$9.000',
    image: 'https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcR-vNSbtMGtj2gj-z5gQ0f-Doi50jlHSov37SfSJ12BBw&s=10',
    tag: 'Vegetariano'
  }
]

const recomendacion = {
  name: 'Volcán de Chocolate Helado',
  description: 'Malteada artesanal de chocolate belga con crema batida, salsa de chocolate caliente y virutas de galleta.',
  price: '$13.900',
  image: 'https://loremflickr.com/600/600/chocolate,milkshake/all?lock=406'
}
</script>
