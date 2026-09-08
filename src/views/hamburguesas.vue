<template>
  <q-page class="q-pa-md q-pa-lg-lg">
    <CategoryBanner
      image="https://images.unsplash.com/photo-1568901346375-23c9450c58cd?auto=format&fit=crop&w=1400&q=80"
      title="🍔 Hamburguesas"
      description="Carne 100% de res, pan brioche horneado y toppings frescos. Nuestras hamburguesas se preparan al momento, a la parrilla."
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
    name: 'Clásica Criolla',
    description: 'Carne de res, queso cheddar, lechuga, tomate, cebolla morada y salsa especial.',
    price: '$18.500',
    image: 'https://images.unsplash.com/photo-1550317138-10000687a72b?auto=format&fit=crop&w=800&q=80',
    tag: 'Más pedido'
  },
  {
    id: 2,
    name: 'BBQ Bacon',
    description: 'Doble carne, tocineta crocante, queso cheddar y salsa BBQ ahumada.',
    price: '$24.900',
    image: 'https://images.unsplash.com/photo-1520072959219-c595dc870360?auto=format&fit=crop&w=800&q=80',
    tag: 'Nuevo'
  },
  {
    id: 3,
    name: 'Jalapeño Fire',
    description: 'Carne de res, queso pepper jack, jalapeños frescos y mayonesa picante.',
    price: '$21.500',
    image: 'https://images.unsplash.com/photo-1561758033-d89a9ad46330?auto=format&fit=crop&w=800&q=80',
    tag: 'Picante'
  },
  {
    id: 4,
    name: 'Veggie Garden',
    description: 'Medallón de garbanzo y vegetales, queso mozzarella, aguacate y rúgula.',
    price: '$19.900',
    image: 'https://images.unsplash.com/photo-1546793665-c74683f339c1?auto=format&fit=crop&w=800&q=80',
    tag: 'Vegetariano'
  }
]

const recomendacion = {
  name: 'Doble Explosión de Queso',
  description: 'Dos carnes de res 100% angus, triple queso fundido, tocineta ahumada y aros de cebolla crocante sobre pan artesanal. La favorita de la casa.',
  price: '$28.900',
  image: 'https://images.unsplash.com/photo-1572802419224-296b0aeee0d9?auto=format&fit=crop&w=900&q=80'
}
</script>
