<script setup>
    import { defineProps, useAttrs, defineEmits } from 'vue';

    const props = defineProps({
        variant: {
            type: String,
            default: 'success'
        }
    })

    const attrs = useAttrs()
    const emit = defineEmits()

    console.log(props.variant)
    console.log(attrs)

    function sendData(){
        emit('update', props.variant)
    }

</script>

<template>
    <button @click="sendData">
        {{ variant}}
        <slot></slot>
        <slot name="icon"></slot>
    </button>
</template>

<style>
</style>