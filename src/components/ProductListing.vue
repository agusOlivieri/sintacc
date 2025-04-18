<script setup>
import ProductModal from './ProductModal.vue';
import { ref } from 'vue';

const props = defineProps({
  image: String,
  title: String,
  description: String,
  type: Number
//   price: Number
});

const mostrarModal = ref(false);

const seleccionarProducto = () => {
  mostrarModal.value = true;
}

const cerrarModal = () => {
  mostrarModal.value = false;
}

</script>

<template>
    <div 
      class="bg-white shadow-lg rounded-2xl border transition-all transform hover:scale-105 hover:shadow-xl view-animate-[--subjectReveal] animate-expand-horizontally animate-range-[entry_10%_contain_5%]"
      :class="type === 0 ? 
      'border-green-400' 
      : 'border-red-400'"
    >
      <button class="hover:cursor-pointer w-full p-5" @click="seleccionarProducto">
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
      </button>

      <teleport to="body">
        <ProductModal v-if="mostrarModal" :titulo="title" :imagen="image" @cerrar="cerrarModal"/>
      </teleport>

    </div>
</template>
  

  