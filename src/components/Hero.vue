<script setup>
defineProps({
    title: String,
    subtitle: String
})
</script>

<template>
    <section id="home" class="bg-emerald-700 py-20 mb-4 text-white">
        <div class="max-w-7xl mx-auto px-4 flex flex-col items-center">
            <div>
                <div class="flex items-center">
                    <h1 class="text-5xl font-extrabold">{{ title }}</h1>
                    <span class="ml-3"><img src="@/assets/images/gluten-free.png" /></span>
                </div>
                <p class="my-4 text-2xl">{{ subtitle }}</p>
            </div>
        </div>
    </section>
</template>