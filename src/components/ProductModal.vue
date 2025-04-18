<script setup>
import { ref } from 'vue';

defineProps({
    titulo: {
        type: String,
    },
    mostrar: {
        type: Boolean,
        required: true
    },
    imagen: {
        type: String,
    }
})

const emit = defineEmits(['cerrar']);

</script>

<template>
    <div class="fixed inset-0 z-10 flex items-center justify-center backdrop-blur-xs animate-blink p-4" @click="$emit('cerrar')">
        <div class="bg-white rounded-lg shadow-lg p-6 max-w-lg w-full">
            <div class="flex justify-between items-center mb-2">
                <h2 class="text-xl ">
                    {{ titulo }}
                </h2>
                <button @click="$emit('cerrar')" class="p-2 pb-1 hover:bg-gray-200 hover:cursor-pointer rounded-lg">
                    <i class="pi pi-times"></i>
                </button>
            </div>
            <img :src="imagen" :alt="title" class="w-full h-72 object-cover rounded-lg" />
            <p class="my-2">
                descripción
            </p>
            <p>
                precio
            </p>
        </div>
    </div>
</template>

