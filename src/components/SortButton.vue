<script setup>
import { ref } from 'vue';

defineProps({
    colors: {
        type: String,
        default: 'bg-gray-200 border-gray-500'
    }
    
})

const productsToShow = ref([]);

const handleSort = () => {

}

</script>

<template>
    <button :class="`${colors} rounded-full p-3 text-sm hover:scale-110 transition-transform duration-200 cursor-pointer border`">
        <slot></slot>
    </button>
</template>