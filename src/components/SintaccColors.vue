<script setup>
import Card from '@/components/Card.vue'
</script>

<template>
    <section id="sintacc-colors" class="mb-4 py-5">
        <div class="grid grid-cols-1 sm:grid-cols-2 gap-4 px-16">
            <Card bg="bg-red-100">
                <div class="flex items-center gap-2">
                    <h2 class="text-2xl font-bold">Productos Rojos</h2>
                    <img src="@/assets/images/gluten-free-red-full.png" width="46" class="rotate-25" />
                </div>
                <p class="mt-2 mb-4">
                    Los productos de color rojo son los que ...
                </p>
            </Card>
            <Card bg="bg-green-100">
                <div class="flex items-center gap-2">
                    <h2 class="text-2xl font-bold">Productos Verdes</h2>
                    <img src="@/assets/images/gluten-free-green-full.png" width="46" class="rotate-25" />
                </div>
                <p class="mt-2 mb-4">
                    Los productos de color verde son los que ...
                </p>
            </Card>
        </div>
    </section>
</template>