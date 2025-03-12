<script setup>
import { RouterLink } from 'vue-router';
</script>

<template>
    <nav class="bg-emerald-700 w-full p-2 text-white border-b-2 border-b-emerald-500">
        <div class="flex justify-between items-center px-5">
            <div id="logo" class="bg-white w-24 h-7">
            </div>
            <div id="buttons" class="flex items-center gap-2">
                <div class="px-2 py-1 hover:bg-emerald-950 text-center rounded-xs">
                    <RouterLink to="/#home">
                        Inicio
                    </RouterLink>
                </div>
                <div class="px-2 py-1 hover:bg-emerald-950 text-center rounded-xs">
                    <RouterLink to="/#products">
                        Productos
                    </RouterLink>
                </div>
            </div>
        </div>
    </nav>
</template>