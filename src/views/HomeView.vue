<template>
    <div class="flex">
        <!-- Navbar -->
        <NavBar />


        <main class="p-4 w-screen md:p-8">
            <h2 class="text-3xl font-bold">Overview</h2>


            <section class="flex flex-col w-full gap-2 mt-8 md:flex-row md:gap-5 md:h-32">
                <div
                    class="h-24 rounded-lg bg-grey900 text-white p-4 flex flex-col justify-between md:w-1/3 md:p-6 md:h-full">
                    <p class="md:text-2xl">Title</p>
                    <p class="text-3xl font-bold">$5,678.45</p>
                </div>
                <div class="h-24 rounded-lg bg-white p-4 flex flex-col justify-between md:w-1/3 md:p-6 md:h-full">
                    <p class="md:text-2xl">Title</p>
                    <p class="text-3xl font-bold">$5,678.45</p>
                </div>
                <div class="h-24 rounded-lg bg-white p-4 flex flex-col justify-between md:w-1/3 md:p-6 md:h-full">
                    <p class="md:text-2xl">Title</p>
                    <p class="text-3xl font-bold">$5,678.45</p>
                </div>
            </section>

            <!-- Pots section -->

        </main>
    </div>
</template>

<script setup lang="ts">
import NavBar from '@/components/nav/NavBar.vue';
</script>