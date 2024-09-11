<script setup lang="ts">
const items = [
  {
    img: 'https://picsum.photos/1920/1080?random=1',
    text: 'Texto para imagen 1'
  },
  {
    img: 'https://picsum.photos/1920/1080?random=2',
    text: 'Texto para imagen 2'
  },
  {
    img: 'https://picsum.photos/1920/1080?random=3',
    text: 'Texto para imagen 3'
  },
  {
    img: 'https://picsum.photos/1920/1080?random=4',
    text: 'Texto para imagen 4'
  },
  {
    img: 'https://picsum.photos/1920/1080?random=5',
    text: 'Texto para imagen 5'
  },
  {
    img: 'https://picsum.photos/1920/1080?random=6',
    text: 'Texto para imagen 6'
  }
]

const carouselRef = ref()

onMounted(() => {
  setInterval(() => {
    if (!carouselRef.value) return

    if (carouselRef.value.page === carouselRef.value.pages) {
      return carouselRef.value.select(0)
    }

    carouselRef.value.next()
  }, 5000)
})
</script>

<template>
  <UCarousel
    ref="carouselRef"
    v-slot="{ item }"
    :items="items"
    :ui="{ item: 'basis-full' }"
    class="max-h-[600px] overflow-hidden relative"
    indicators
  >
    <!-- Contenedor de la imagen y el texto superpuesto -->
    <div class="relative w-full h-full flex items-center justify-center">
      <img :src="item.img" class="w-full h-full object-cover" draggable="false">

      <!-- Texto superpuesto -->
      <div class="absolute  w-full p-4 text-white text-2xl text-center font-bold">
        {{ item.text }}
      </div>
    </div>
  </UCarousel>
</template>
