<template>
    <li @click="$emit('click')" :class="[
        'cursor-pointer flex flex-col items-center justify-center h-full w-12 md:w-32 mt-2 rounded-t-lg pb-1    lg:w-full lg:h-14 lg:mr-10 lg:rounded-l-none lg:rounded-r-lg lg:flex-row lg:justify-start',
        isActive ? 'bg-white text-grey900' : 'bg-grey900 text-grey300',
    ]">
        <component :is="icon" class="w-6 md:w-10 lg:ml-16" />
        <p class="hidden md:block font-bold lg:ml-4">{{ title }}</p>
    </li>
</template>

<script setup lang="ts">
import { defineProps } from 'vue';

defineProps({
    icon: {
        type: Function,
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