<template>
  <q-card class="chef-card q-mt-lg" flat bordered style="max-width: 640px; margin-left: auto; margin-right: auto;">
    <div class="row items-stretch no-wrap">
      <div class="col-4" style="max-width: 180px;">
        <q-img :src="product.image" class="full-height" :ratio="1" />
      </div>
      <div class="col">
        <q-card-section class="column full-height justify-between q-pa-sm-sm q-pa-md">
          <div>
            <div class="row items-center q-gutter-x-xs">
              <q-icon name="restaurant_menu" color="warning" size="16px" />
              <span class="text-caption text-weight-bold text-uppercase" style="color: #F4A300; letter-spacing: .5px; font-size: 11px;">
                Recomendado
              </span>
            </div>
            <div class="text-subtitle1 font-title text-weight-bold q-mt-xs">{{ product.name }}</div>
            <div class="text-caption text-grey-8 q-mt-xs" style="display: -webkit-box; -webkit-line-clamp: 2; -webkit-box-orient: vertical; overflow: hidden;">
              {{ product.description }}
            </div>
          </div>

          <div class="row items-center justify-between q-mt-sm">
            <div class="text-subtitle1 text-weight-bold" style="color: #E63946;">
              {{ product.price }}
            </div>
            <q-btn round color="primary" icon="add_shopping_cart" size="xs" />
          </div>
        </q-card-section>
      </div>
    </div>
  </q-card>
</template>

<script setup>
defineProps({
  product: { type: Object, required: true }
})
</script>
