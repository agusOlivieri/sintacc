<script setup>
defineProps({
  image: String,
  title: String,
  description: String,
//   price: Number
});
</script>

<template>
    <div class="bg-white shadow-lg rounded-2xl p-4 border border-gray-200">
      <img :src="image" :alt="title" class="w-full h-40 object-cover rounded-xl" />
      
      <div class="mt-4">
        <h2 class="text-xl font-bold text-red-600">{{ title }}</h2>
        <p class="text-gray-700 text-sm mt-2">{{ description }}</p>
      </div>
  
      <!-- <div class="mt-4 flex justify-between items-center">
        <span class="text-green-600 font-semibold text-lg">${{ price }}</span>
        <button class="bg-red-500 text-white px-4 py-2 rounded-lg hover:bg-red-600 transition">
          Comprar
        </button>
      </div> -->
    </div>
  </template>
  

  