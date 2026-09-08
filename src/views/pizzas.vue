<template>
  <q-page class="q-pa-md q-pa-lg-lg">
    <CategoryBanner
      image="https://loremflickr.com/1200/400/pizza,margherita/all?lock=301"
      title="🍕 Pizzas"
      description="Masa artesanal fermentada 24 horas, horneada en piedra y cubierta con ingredientes frescos seleccionados."
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
    name: 'Pizza Margarita',
    description: 'Salsa de tomate, mozzarella fresca, albahaca y un toque de aceite de oliva.',
    price: '$26.000',
    image: 'https://loremflickr.com/500/400/pizza,margherita/all?lock=302',
    tag: 'Más pedido'
  },
  {
    id: 2,
    name: 'Pizza Hawaiana',
    description: 'Jamón, piña asada, mozzarella y un toque de orégano.',
    price: '$28.500',
    image: 'https://loremflickr.com/500/400/pizza,hawaiian/all?lock=303',
    tag: 'Nuevo'
  },
  {
    id: 3,
    name: 'Pizza Diabla',
    description: 'Pepperoni picante, jalapeños, salsa diabla y queso mozzarella.',
    price: '$29.900',
    image: 'https://loremflickr.com/500/400/pizza,pepperoni/all?lock=304',
    tag: 'Picante'
  },
  {
    id: 4,
    name: 'Pizza Vegetariana',
    description: 'Champiñones, pimentón, cebolla morada, aceitunas y espinaca fresca.',
    price: '$27.500',
    image: 'https://loremflickr.com/500/400/pizza,vegetable/all?lock=305',
    tag: 'Vegetariano'
  }
]

const recomendacion = {
  name: 'Pizza Cuatro Quesos Especial',
  description: 'Mozzarella, parmesano, gorgonzola y queso crema sobre base artesanal, gratinada al horno de piedra y terminada con miel de abeja.',
  price: '$32.900',
  image: 'https://loremflickr.com/600/600/pizza,cheese/all?lock=306'
}
</script>
