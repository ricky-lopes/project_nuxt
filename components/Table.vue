<script setup>
    const people = [
        {
            id: 1,
            Nome: 'Lindsay Walton',
            Idade: '20',
            email: 'lindsay.walton@example.com',
            role: 'Member'
        },
        {
            id: 2,
            Nome: 'Courtney Henry',
            Idade: '20',
            email: 'courtney.henry@example.com',
            role: 'Admin'
        }, 
        {
            id: 3,
            Nome: 'Tom Cook',
            Idade: '20',
            email: 'tom.cook@example.com',
            role: 'Member'
        }, 
        {
            id: 4,
            Nome: 'Whitney Francis',
            Idade: '20',
            email: 'whitney.francis@example.com',
            role: 'Admin'
        }, 
        {
            id: 5,
            Nome: 'Leonard Krasner',
            Idade: '20',
            email: 'leonard.krasner@example.com',
            role: 'Owner'
        }, 
        {
            id: 6,
            Nome: 'Floyd Miles',
            Idade: '20',
            email: 'floyd.miles@example.com',
            role: 'Member'
        }
    ]

    const page = ref(1)
    const pageCount = 5

    const rows = computed(() => {
        return people.slice((page.value - 1) * pageCount, (page.value) * pageCount)
    })
</script>

<template>
    <div>
        <UTable :rows="filteredRows ?? rows" />

        <UPagination v-model="page" :page-count="pageCount" :total="people.length" />
    </div>
</template>