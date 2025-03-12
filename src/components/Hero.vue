<script setup>
defineProps({
    title: String,
    subtitle: String
})
</script>

<template>
    <section id="home" class="bg-emerald-700 py-20 mb-4 text-white">
        <div class="max-w-7xl mx-auto px-4 flex flex-col items-center">
            <div class="text-center">
                <h1 class="text-4xl font-extrabold">{{ title }}
                    <span class="inline-flex items-center ml-2"><img src="@/assets/images/sintacc-logo.png" width="46" /></span>
                </h1>
                <p class="my-4 text-xl">{{ subtitle }}</p>
            </div>
        </div>
    </section>
</template>