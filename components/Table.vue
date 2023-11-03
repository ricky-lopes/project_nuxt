<script setup>
    const props = defineProps(['data'])

    const page = ref(1)
    const pageCount = 5

    const rows = computed(() => {
        return props.data.slice((page.value - 1) * pageCount, (page.value) * pageCount)
    })
</script>

<template>
    <div>
        <UTable :rows="rows" />

        <UPagination v-model="page" :page-count="pageCount" :total="props.data.length" :active-button="{ color: 'red' }" :inactive-button="{ color: 'gray' }"/>
    </div>
</template>