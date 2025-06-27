<template>
  <aside class="bg-white w-full md:w-60 min-h-screen p-6 shadow-md flex-shrink-0 border-r border-gray-200">
    <nav class="space-y-2">
      <RouterLink
        to="/"
        class="block py-2 px-3 rounded-lg transition bg-gradient-to-l from-blue-50 hover:from-indigo-100 hover:text-blue-700 font-semibold"
        exact-active-class="bg-blue-100 text-blue-700"
      >Home</RouterLink>
      <RouterLink
        to="/about"
        class="block py-2 px-3 rounded-lg transition bg-gradient-to-l from-blue-50 hover:from-indigo-100 hover:text-blue-700 font-semibold"
        exact-active-class="bg-blue-100 text-blue-700"
      >About</RouterLink>
      <RouterLink
        to="/contact"
        class="block py-2 px-3 rounded-lg transition bg-gradient-to-l from-blue-50 hover:from-indigo-100 hover:text-blue-700 font-semibold"
        exact-active-class="bg-blue-100 text-blue-700"
      >Contact</RouterLink>
      <RouterLink
        to="/gallery"
        class="block py-2 px-3 rounded-lg transition bg-gradient-to-l from-blue-50 hover:from-indigo-100 hover:text-blue-700 font-semibold"
        exact-active-class="bg-blue-100 text-blue-700"
      >Gallery</RouterLink>
    </nav>
  </aside>
</template>
