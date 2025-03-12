<script setup>
import Card from '@/components/Card.vue'
</script>

<template>
    <section id="sintacc-colors">
        <div class="flex items-center gap-x-3 justify-center">
            <Card bg="bg-red-100">
                <h2 class="text-2xl font-bold">Productos Rojos</h2>
                <p class="mt-2 mb-4">
                    Los productos de color rojo son los que ...
                </p>
            </Card>
            <Card bg="bg-green-100">
                <h2 class="text-2xl font-bold">Productos verdes</h2>
                <p class="mt-2 mb-4">
                    Los productos de color verde son los que ...
                </p>
            </Card>
        </div>
    </section>
</template>