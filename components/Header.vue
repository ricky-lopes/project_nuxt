<template>
    <div class="flex w-full bg-red-600 h-8 p-8 justify-between items-center shadow-2xl">
        <USlideover :side="'left'" v-model="isOpen">
        <div class="bg-red-600 p-4 flex-1">
            <Placeholder class="h-full" />
            <div class="flex flex-col">
                <div class="w-full flex justify-between items-center mb-4">
                    <h1 class="font-bold text-white">GymTech Personal</h1>
                    <button class="close-img">
                        <h2 class="font-bold text-white px-1 rounded hover:text-red-800" @click="isOpen = false">X</h2>
                    </button>
                </div>
                <nuxt-link v-for="menu in menus" class="p-2 text-white hover:bg-red-800 rounded" @click="isOpen = false" :to="menu.route">{{ menu.name }}</nuxt-link>
            </div>
        </div>
            </USlideover>
        <div class="flex gap-6">
            <UButton class="hover:bg-red-800 rounded" :color="'text-red-600'" :icon="'i-heroicons-bars-3'" @click="isOpen = true" />
            <nuxt-link class="text-white" to="/">
                <h1 class="font-bold text-white">GymTech Personal</h1>
            </nuxt-link>
        </div>

    </div>
</template>

<script setup>
    import {menus} from '~/data/menu.json'

    const isOpen = ref(false)
</script>