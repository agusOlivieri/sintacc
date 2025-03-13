<script setup>
defineProps({
    title: String,
    subtitle: String
})
</script>

<template>
    <section id="home" class="bg-emerald-700 py-20 mb-4 text-white">
        <div class="max-w-7xl px-4 flex flex-col items-center">
            <div>
                <div class="flex items-center gap-4 flex-wrap justify-center">
                    <h1 class="text-2xl font-extrabold sm:text-5xl">{{ title }}</h1>
                    <img src="@/assets/images/gluten-free.png" class="sm:w-32 w-18"/>
                </div>
                <p class="my-4 sm:text-2xl">{{ subtitle }}</p>
            </div>
        </div>
    </section>
</template>