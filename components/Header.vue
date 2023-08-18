<template>
    <div class="flex w-full bg-green-600 h-8 p-8 justify-between items-center shadow-2xl">
        <nuxt-link class="text-white" to="/">
            <h1 class="font-bold text-white">Julia Zeinade Personal</h1>
        </nuxt-link>

        <div class="flex gap-6">
            <nuxt-link class="text-white hover:underline" to="/Alunos">Alunos</nuxt-link>

            <nuxt-link class="text-white hover:underline" to="/Aparelhos">Aparelhos</nuxt-link>

            <nuxt-link class="text-white hover:underline" to="/Treinos">Meus Treinos</nuxt-link>
        </div>
    </div>
</template>