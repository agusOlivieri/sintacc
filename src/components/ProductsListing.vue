<script setup>
import ProductListing from '@/components/ProductListing.vue';
import SortButton from '@/components/SortButton.vue';
import { ref } from 'vue';

const products = ref([
  {
    image: "@/assets/images/food-images/medialunas.jpg",
    title: "Medialunas",
    description: "Harina sin TACC, ideal para repostería y recetas saludables.",
    type: 0
  },
  {
    image: "https://via.placeholder.com/150",
    title: "Galletas de Arroz",
    description: "Crujientes galletas sin gluten, perfectas para acompañar meriendas.",
    type: 0
  },
  {
    image: "https://via.placeholder.com/150",
    title: "Fideos de Maíz",
    description: "Pasta sin gluten hecha a base de maíz, de fácil digestión.",
    type: 1
  },
  {
    image: "https://via.placeholder.com/150",
    title: "Pan de Mandioca",
    description: "Pan sin TACC, esponjoso y con un sabor suave.",
    type: 1
  },
  {
    image: "https://via.placeholder.com/150",
    title: "Chocolatada Sin Azúcar",
    description: "Deliciosa chocolatada sin TACC, sin azúcar añadida.",
    type: 0
  },
  {
    image: "https://via.placeholder.com/150",
    title: "Barra de Cereal",
    description: "Barrita sin gluten con frutos secos y miel.",
    type: 0
  },
  {
    image: "https://via.placeholder.com/150",
    title: "Mermelada de Frutas",
    description: "Mermelada sin conservantes ni gluten, endulzada naturalmente.",
    type: 1
  },
  {
    image: "https://via.placeholder.com/150",
    title: "Mix de Frutos Secos",
    description: "Combinación de almendras, nueces y pasas sin gluten.",
    type: 1
  }
]);

const filteredProducts = ref([...products.value])

const filterProducts = (type) => {
  filteredProducts.value = [];
  setTimeout(() => {
    filteredProducts.value = type === 'all' 
      ? [...products.value] 
      : products.value.filter(p => p.type === type);
  }, 200);
};

</script>

<template>
    <section id="products" class="bg-gray-100 px-6 py-10">
        <div class="max-w-6xl mx-auto text-center">

            <h2 class="text-2xl sm:text-4xl font-extrabold mb-4 text-gray-800">
                Descubre Nuestra Selección
            </h2>

            <p class="sm:text-lg text-gray-600 mb-12 max-w-2xl mx-auto">
              Alimentos sin TACC de la mejor calidad, cuidadosamente seleccionados para tu bienestar.
            </p>

            <div class="mb-8 flex gap-6">
              <SortButton @click="filterProducts('all')">
                Todos
              </SortButton>
              <SortButton colors="bg-red-200 border-red-500" @click="filterProducts(1)">
                Con Lacteos
              </SortButton>
              <SortButton colors="bg-green-200 border-green-500" @click="filterProducts(0)">
                Sin Lacteos
              </SortButton>
            </div>

            <transition-group 
                tag="div" 
                name="fade" 
                class="grid grid-cols-1 sm:grid-cols-2 gap-8"
            >
                <ProductListing 
                    v-for="product in filteredProducts"
                    :key="product.title"
                    :image="product.image"
                    :title="product.title"
                    :description="product.description"
                    :type="product.type"
                />
            </transition-group>
        </div>
    </section>
</template>

<style scoped>
.fade-enter-active, .fade-leave-active {
  transition: opacity 0.5s ease-in-out, transform 0.5s ease-in-out;
}

.fade-enter-from {
  opacity: 0;
  transform: translateY(10px);
}

.fade-leave-to {
  opacity: 0;
  transform: translateY(-10px);
}
</style>