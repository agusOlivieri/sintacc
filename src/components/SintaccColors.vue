<script setup>
import Card from '@/components/Card.vue'
</script>

<template>
    <section id="sintacc-colors" class="my-18 pb-4 text-center">
        <h2 class="text-xl sm:text-3xl font-bold text-gray-800 mb-8">
            ¿Qué significan los colores en nuestros productos?
        </h2>

        <div class="grid grid-cols-1 sm:grid-cols-2 gap-6 px-6 md:px-16">
            <Card colors="bg-red-100 border-red-500 view-animate-[--subjectReveal] animate-zoom-in animate-range-[entry_10%_contain_25%]">
                <div class="flex items-center gap-2">
                    <h3 class="text-2xl font-bold text-red-700">Productos Rojos</h3>
                    <img src="@/assets/images/gluten-free-red-full.png" width="46" class="rotate-6" />
                </div>
                <p class="mt-2 mb-4">
                    🥛 Los productos de color rojo contienen **lactosa**.
                </p>
            </Card>
            <Card colors="bg-green-100 border-green-500 view-animate-[--subjectReveal] animate-zoom-in animate-range-[entry_10%_contain_45%]">
                <div class="flex items-center gap-2">
                    <h3 class="text-2xl font-bold text-green-700">Productos Verdes</h3>
                    <img src="@/assets/images/gluten-free-green-full.png" width="46" class="-rotate-6" />
                </div>
                <p class="mt-2 mb-4">
                    🌱 Los productos de color verde **no contienen lactosa**.
                </p>
            </Card>
        </div>
    </section>
</template>