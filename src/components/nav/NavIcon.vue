<template>
    <li @click="$emit('click')" :class="[
        'cursor-pointer flex flex-col items-center justify-center w-12 h-12',
        isActive ? 'bg-white text-grey900' : 'bg-grey900 text-grey300',
    ]">
        <component :is="icon" class="h-6 w-6" />
    </li>
</template>

<script setup lang="ts">
import { defineProps } from 'vue';

defineProps({
    icon: {
        type: Object,
        required: true,
    },
    isActive: {
        type: Boolean,
        required: true,
    },
});
</script>