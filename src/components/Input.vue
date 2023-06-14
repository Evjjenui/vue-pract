<script setup>
    defineProps(['modelValue'])
    defineEmits(['update:modelValue'])
</script>
<template>
    <form @submit="console.log('submit')">
        <input
            :value="modelValue"
            type="text"
            @input="$emit('update:modelValue', $event.target.value)">
        <button type="submit">Add</button>
    </form>
</template>