<template>
  <Layout>
    <h2 class="text-2xl font-bold mb-4 text-blue-700">Gallery</h2>
    <p class="mb-6 text-gray-600">Klik gambar untuk memperbesar.</p>
    <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-4 gap-6">
      <div
        v-for="(img, idx) in images"
        :key="idx"
        class="rounded-2xl shadow-lg overflow-hidden hover:scale-105 transition-transform group cursor-pointer bg-white"
        @click="openZoom(img)"
      >
        <img
          :src="img"
          :alt="'Gambar ' + (idx + 1)"
          class="w-full h-40 object-cover group-hover:brightness-110 transition"
        />
      </div>
    </div>

    <!-- Modal Zoom -->
    <div
      v-if="zoomImage"
      class="fixed inset-0 bg-black bg-opacity-70 z-50 flex items-center justify-center transition"
      @click.self="closeZoom"
    >
      <div class="relative max-w-2xl w-full p-4">
        <img
          :src="zoomImage"
          alt="Zoom"
          class="w-full max-h-[80vh] rounded-2xl shadow-2xl object-contain bg-white"
        />
        <button
          class="absolute -top-2 -right-2 bg-white rounded-full p-2 shadow hover:bg-blue-100 transition"
          @click="closeZoom"
        >
          <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 text-gray-700" fill="none" viewBox="0 0 24 24" stroke="currentColor">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12" />
          </svg>
        </button>
      </div>
    </div>
  </Layout>
</template>

<script setup>
import { ref } from 'vue'
import Layout from '@/layouts/Layout.vue'

const images = [
  'https://images.unsplash.com/photo-1506744038136-46273834b3fb?auto=format&fit=crop&w=400&q=80',
  'https://images.unsplash.com/photo-1519125323398-675f0ddb6308?auto=format&fit=crop&w=400&q=80',
  'https://images.unsplash.com/photo-1465101046530-73398c7f28ca?auto=format&fit=crop&w=400&q=80',
  'https://images.unsplash.com/photo-1500534314209-a25ddb2bd429?auto=format&fit=crop&w=400&q=80'
]

const zoomImage = ref(null)
function openZoom(img) {
  zoomImage.value = img
}
function closeZoom() {
  zoomImage.value = null
}
</script>
