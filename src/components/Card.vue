<script setup>

defineProps({
    colors: {
        type: String,
        default: 'bg-gray-100 border-gray-500'
    }
})
</script>

<template>
    <div :class="`${colors} p-6 rounded-lg shadow-md border-l-4 hover:scale-105 transition-transform duration-300`">
        <slot></slot>
    </div>
</template>