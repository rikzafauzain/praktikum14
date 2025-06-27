<template>
  <div class="min-h-screen bg-gradient-to-br from-blue-50 via-white to-indigo-100">
    <Header />
    <div class="flex flex-col md:flex-row">
      <Sidebar />
      <main class="flex-1 p-8">
        <div class="bg-white shadow-xl rounded-3xl p-8 min-h-[80vh]">
          <slot />
        </div>
      </main>
    </div>
  </div>
</template>

<script setup>
import Header from '@/components/Header.vue'
import Sidebar from '@/components/Sidebar.vue'
</script>
