<template>
  <q-page class="q-pa-md q-pa-lg-lg">
    <CategoryBanner
      image="https://loremflickr.com/1200/400/restaurant,kitchen/all?lock=701"
      title="👨‍🍳 Nosotros"
      description="Conoce nuestra historia, dónde estamos y quiénes hacen posible cada pedido."
    />

    <div class="row q-col-gutter-lg">
      <!-- Historia -->
      <div class="col-12 col-md-7">
        <q-card flat bordered class="q-pa-md" style="border-radius: 16px;">
          <div class="text-h6 font-title text-weight-bold q-mb-sm">
            <q-icon name="menu_book" color="primary" class="q-mr-xs" />
            Nuestra historia
          </div>
          <p class="text-body1 text-grey-9">
            Nacimos en 2015 en un pequeño local de barrio con una idea simple: servir comida
            rápida hecha con ingredientes de verdad. Empezamos con una parrilla y cinco
            recetas de hamburguesas; hoy preparamos hamburguesas, perros calientes, pizzas,
            bebidas y postres para toda la ciudad, sin perder la receta original que nos
            hizo crecer: cocinar cada pedido como si fuera para nuestra propia familia.
          </p>
        </q-card>

        <q-card flat bordered class="q-pa-md q-mt-md" style="border-radius: 16px;">
          <div class="text-h6 font-title text-weight-bold q-mb-sm">
            <q-icon name="place" color="primary" class="q-mr-xs" />
            Dirección y horarios
          </div>
          <p class="text-body1 text-grey-9 q-mb-xs">
            <strong>Dirección:</strong> Calle 45 # 20-30, Bucaramanga, Santander.
          </p>
          <p class="text-body1 text-grey-9">
            <strong>Horario de atención:</strong><br>
            Lunes a jueves: 11:00 a.m. – 9:00 p.m.<br>
            Viernes a domingo: 11:00 a.m. – 11:00 p.m.
          </p>
        </q-card>

        <q-card flat bordered class="q-pa-md q-mt-md" style="border-radius: 16px;">
          <div class="text-h6 font-title text-weight-bold q-mb-sm">
            <q-icon name="phone" color="primary" class="q-mr-xs" />
            Contacto y pedidos
          </div>
          <p class="text-body1 text-grey-9 q-mb-xs">
            <strong>Teléfono:</strong> (607) 634 00 00
          </p>
          <p class="text-body1 text-grey-9">
            <strong>WhatsApp de pedidos:</strong> 300 123 45 67
          </p>
          <q-btn
            color="positive"
            icon="chat"
            label="Pedir por WhatsApp"
            unelevated
            rounded
            class="q-mt-sm"
            href="https://wa.me/573001234567"
            target="_blank"
          />
        </q-card>
      </div>

      <!-- Equipo -->
      <div class="col-12 col-md-5">
        <div class="text-h6 font-title text-weight-bold q-mb-md text-center">Nuestro equipo</div>
        <div class="row q-col-gutter-md">
          <div v-for="member in equipo" :key="member.name" class="col-12">
            <q-card flat bordered class="row items-center q-pa-sm" style="border-radius: 16px;">
              <q-avatar size="72px" class="team-avatar q-ma-sm">
                <img :src="member.photo">
              </q-avatar>
              <div class="q-ml-sm">
                <div class="text-subtitle1 text-weight-bold">{{ member.name }}</div>
                <div class="text-caption text-grey-8">{{ member.role }}</div>
              </div>
            </q-card>
          </div>
        </div>
      </div>
    </div>
  </q-page>
</template>

<script setup>
import CategoryBanner from '../components/CategoryBanner.vue'

const equipo = [
  {
    name: 'Andrés Gómez',
    role: 'Chef principal',
    photo: 'https://i.pravatar.cc/150?img=12'
  },
  {
    name: 'Laura Martínez',
    role: 'Cajera',
    photo: 'https://i.pravatar.cc/150?img=47'
  },
  {
    name: 'Camilo Rojas',
    role: 'Domiciliario',
    photo: 'https://i.pravatar.cc/150?img=33'
  }
]
</script>
