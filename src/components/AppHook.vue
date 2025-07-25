<script setup>
    import { onBeforeMount, onMounted, onBeforeUnmount, onUnmounted } from 'vue';

    onBeforeMount(() => {
        console.log('onBeforeMount')
    })

    onMounted(() => {
        console.log('onMounted')
    })

    onBeforeUnmount(() => {
        console.log('onBeforeUnmount')
    })

    onUnmounted(() => {
        console.log('onUnmounted')
    })

</script>

<template>
    <div>
        app hook
    </div>
</template>

<style>

</style>