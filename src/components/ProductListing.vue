<script setup>
const props = defineProps({
  image: String,
  title: String,
  description: String,
  type: Number
//   price: Number
});

console.log(props.image);

const getImagePath = (fileName) => {
  return new URL(`@/assets/images/food-images/${fileName}`, import.meta.url).href;
};

</script>

<template>
    <div 
      class="bg-white shadow-lg rounded-2xl p-5 border transition-all transform hover:scale-105 hover:shadow-xl  view-animate-[--subjectReveal] animate-expand-horizontally animate-range-[entry_10%_contain_5%]"
      :class="type === 0 ? 
      'border-green-400' 
      : 'border-red-400'"
    >
      <img :src="image" :alt="title" class="w-full h-72 object-cover rounded-lg" />
      
      <div class="mt-4">
        <div class="flex items-center gap-3">
          <h2 
            class="text-xl font-bold text-green-600"
            :class="type === 0 ? 'text-green-600' : 'text-red-600'"
          >
            {{ title }}
          </h2>
          <img v-if="type === 0"
            src="@/assets/images/gluten-free-green-full.png" 
            class="w-10 animate-bounce rotate-6"
          />
          <img v-else
            src="@/assets/images/gluten-free-red-full.png" 
            class="w-10 animate-bounce -rotate-6"
          />
        </div>
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
  

  