<script setup>
defineProps({
    title: String,
    subtitle: String
})
</script>

<template>
    <!-- <section id="home" class=" bg-cover bg-center bg-[url('@/assets/images/fondo_sintacc.avif')] py-20 text-white"> -->
    <section id="home" class="bg-gradient-to-r from-emerald-700 to-emerald-600 py-20 text-white">
        <div class="max-w-4xl mx-auto px-6 text-center">
            
            <div class="flex flex-col items-center justify-center gap-4">
                <h1 class="mb-6 text-2xl font-extrabold sm:text-5xl">{{ title }}</h1>
                <!-- <img src="@/assets/images/delicias_sintacc_removedbg.png" class="w-20 sm:w-64 transition-transform duration-300 hover:scale-110" alt="Gluten Free Logo" /> -->
                <img src="@/assets/images/delicias_sintacc_removedbg.png" class="rounded-full w-28 sm:w-56" />
                <p class="mt-6 text-lg sm:text-2xl leading-relaxed max-w-2xl mx-auto">{{ subtitle }}</p>
            </div>

        </div>
    </section>
</template>