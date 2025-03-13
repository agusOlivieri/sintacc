<script setup>
import ProductListing from '@/components/ProductListing.vue';

const products = [
  {
    image: "https://via.placeholder.com/150",
    title: "Harina de Almendra",
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
];

</script>

<template>
    <section id="products" class=" bg-blue-50 px-4 py-10">
        <div class="container-xl m-auto">
            <h2 class="text-3xl font-bold mb-10 text-center">
                Nuestros Productos
            </h2>
            <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 gap-6">
                <ProductListing 
                    v-for="product in products"
                    :image="product.image"
                    :title="product.title"
                    :description="product.description"
                    :type="product.type"
                />
            </div>
        </div>
    </section>
</template>