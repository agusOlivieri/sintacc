<script setup>
import ProductListing from '@/components/ProductListing.vue';
import SortButton from '@/components/SortButton.vue';
import { ref } from 'vue';

const images = import.meta.glob('@/assets/images/food-images/*.{jpg,jpeg,png,gif}', {
  eager: true,
  import: 'default'
});

const products = ref([
  {
    image: "medialunas.jpg",
    title: "Medialunas",
    description: "-",
    type: 0
  },
  {
    image: "galletas_membrillo.jpg",
    title: "Galletas con membrillo",
    description: "-",
    type: 0
  },
  {
    image: "ravioles.jpg",
    title: "Ravioles",
    description: "-",
    type: 1
  },
  {
    image: "bizcochitos.jpg",
    title: "Bizcochitos",
    description: "-",
    type: 1
  },
  {
    image: "chipa.jpg",
    title: "Chipá",
    description: "-",
    type: 0
  },
  {
    image: "pastafrola.jpg",
    title: "Pastafrola",
    description: "-",
    type: 0
  },
  {
    image: "pastafrola_membrillo.jpg",
    title: "Pastafrola de membrillo",
    description: "-",
    type: 1
  },
  {
    image: "alfajores_negros.jpg",
    title: "Alfajores negros",
    description: "-",
    type: 1
  },
  {
    image: "alfajores_maicena.jpg",
    title: "Alfajores de maicena",
    description: "-",
    type: 1
  }
]);

const productsWithImages = products.value.map(product => ({
  ...product,
  image: images[`/src/assets/images/food-images/${product.image}`]
}));

const filteredProducts = ref([...productsWithImages])

const filterProducts = (type) => {
  filteredProducts.value = [];
  setTimeout(() => {
    filteredProducts.value = type === 'all' 
      ? [...productsWithImages] 
      : productsWithImages.filter(p => p.type === type);
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