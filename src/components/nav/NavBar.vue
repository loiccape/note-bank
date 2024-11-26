<template>
    <nav
        class="bg-grey900 fixed bottom-0 w-full h-12 lg:fixed lg:top-0 lg:bottom-auto lg:h-screen  lg:left-0 lg:flex lg:flex-col lg:w-1/6 lg:rounded-r-lg">
        <img src="../../assets/images/logo-large.svg" alt="logo finance"
            class="hidden lg:block lg:w-32 lg:mt-12 lg:ml-12" />

        <ul
            class="w-full h-full flex justify-evenly items-center text-grey300 lg:flex lg:flex-col lg:justify-normal lg:mt-16">
            <!-- Boucle sur les icônes pour les rendre dynamiques si besoin -->
            <NavIcon :icon="DocumentTextIcon" title="Overview" :index="1" :isActive="activeIndex === 1"
                @click="handleClick(1)" />
            <NavIcon :icon="HomeIcon" title="Transactions" :index="2" :isActive="activeIndex === 2"
                @click="handleClick(2)" />
            <NavIcon :icon="AdjustmentsVerticalIcon" title="Budgets" :index="3" :isActive="activeIndex === 3"
                @click="handleClick(3)" />
            <NavIcon :icon="ChartPieIcon" title="Pots" :index="4" :isActive="activeIndex === 4"
                @click="handleClick(4)" />
            <NavIcon :icon="WalletIcon" title="Recurring bills" :index="5" :isActive="activeIndex === 5"
                @click="handleClick(5)" />
        </ul>
    </nav>
</template>

<script setup lang="ts">
import { ref } from 'vue';
import {
    DocumentTextIcon,
    HomeIcon,
    AdjustmentsVerticalIcon,
    ChartPieIcon,
    WalletIcon,
} from '@heroicons/vue/16/solid';
import NavIcon from './NavIcon.vue';

// Suivre l'index actif
const activeIndex = ref<number>(0);

// Gérer le clic
const handleClick = (index: number) => {
    activeIndex.value = index;
};
</script>