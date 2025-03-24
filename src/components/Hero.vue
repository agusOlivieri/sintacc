<script setup>
defineProps({
    title: String,
    subtitle: String
})
</script>

<template>
    <!-- <section id="home" class=" bg-cover bg-center bg-[url('@/assets/images/fondo_sintacc.avif')] py-20 text-white"> -->
    <section id="home" class="bg-gradient-to-r from-emerald-700 to-emerald-600 py-20 text-white">
        <div class="max-w-6xl mx-auto px-6 text-center">
            
            <div class="flex felx-col items-center justify-center gap-4">
                <h1 class="text-2xl font-extrabold sm:text-5xl">{{ title }}</h1>
                <img src="@/assets/images/gluten-free.png" class="w-20 sm:w-32 transition-transform duration-300 hover:scale-110" alt="Gluten Free Logo" />
            </div>
            
            <p class="mt-6 text-lg sm:text-2xl opacity-90 leading-relaxed max-w-2xl mx-auto">{{ subtitle }}</p>
        </div>
    </section>
</template>