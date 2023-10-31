<template>
    <div class="flex w-full bg-red-600 h-8 p-8 justify-between items-center shadow-2xl">
        <USlideover v-model="isOpen">
        <div class="p-4 flex-1">
            <Placeholder class="h-full" />
            <div class="gap-6">
                <nuxt-link class="text-red-600 font-bold hover:underline" @click="isOpen = false" to="/Alunos">Alunos</nuxt-link>
                <br>
                <nuxt-link class="text-red-600 font-bold hover:underline" @click="isOpen = false" to="/Aparelhos">Aparelhos</nuxt-link>
                <br>
                <nuxt-link class="text-red-600 font-bold hover:underline" @click="isOpen = false" to="/Treinos">Treinos</nuxt-link>
            </div>
        </div>
            </USlideover>
        <div class="flex gap-6">
            <UButton label="Open" @click="isOpen = true" />
            <nuxt-link class="text-white" to="/">
                <h1 class="font-bold text-white">Gym Tech Personal</h1>
            </nuxt-link>
        </div>

    </div>
</template>

<script setup>
    const isOpen = ref(false)
</script>