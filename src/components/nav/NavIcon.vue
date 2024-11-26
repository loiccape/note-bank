<template>
    <li @click="$emit('click')" :class="[
        'cursor-pointer flex flex-col items-center justify-center h-full w-12 md:w-32 mt-2 rounded-t-lg',
        isActive ? 'bg-white text-grey900' : 'bg-grey900 text-grey300',
    ]">
        <component :is="icon" class="w-6 md:w-10" />
        <p class="hidden md:block font-bold">{{ title }}</p>
    </li>
</template>

<script setup lang="ts">
import { defineProps } from 'vue';

defineProps({
    icon: {
        type: Object,
        required: true,
    },
    title: {
        type: String,
        required: true
    },
    isActive: {
        type: Boolean,
        required: true,
    },
});
</script>