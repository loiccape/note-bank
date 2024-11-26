<template>
    <div class="flex">
        <!-- Navbar -->
        <NavBar />


        <main class="p-4 w-screen md:p-8 lg:p-12 mb-16 lg:m-0">
            <h2 class="text-3xl font-bold">Overview</h2>


            <section class="flex flex-col w-full gap-2 mt-8 md:flex-row md:gap-5 md:h-32">
                <div
                    class="h-24 rounded-lg bg-grey900 text-white p-4 flex flex-col justify-between md:w-1/3 md:p-6 md:h-full">
                    <p class="md:text-2xl">Current Balance</p>
                    <p class="text-3xl font-bold">$5,678.45</p>
                </div>
                <div class="h-24 rounded-lg bg-white p-4 flex flex-col justify-between md:w-1/3 md:p-6 md:h-full">
                    <p class="md:text-2xl">Income</p>
                    <p class="text-3xl font-bold">$5,678.45</p>
                </div>
                <div class="h-24 rounded-lg bg-white p-4 flex flex-col justify-between md:w-1/3 md:p-6 md:h-full">
                    <p class="md:text-2xl">Expenses</p>
                    <p class="text-3xl font-bold">$5,678.45</p>
                </div>
            </section>

            <!-- Pots section -->
            <section class="bg-white rounded-lg p-4 mt-10">
                <div class="flex justify-between items-center">
                    <h2 class="text-2xl font-bold">Pots</h2>
                    <a href="/" class="text-grey500">See Details</a>
                </div>


                <div class="bg-beige100 mt-3 rounded-lg p-4 flex items-center min-h-24">
                    <WalletIcon class="text-green-900 w-9 mr-4" />
                    <div>
                        <p class="text-grey500">Total Saved</p>
                        <p class="text-2xl font-bold">$890</p>
                    </div>
                </div>


                <div class="grid grid-cols-2 gap-4 mt-10">
                    <div class="border-l-4 border-green-900 pl-4">
                        <p>Title</p>
                        <p class="">$456</p>
                    </div>
                    <div class="border-l-4 border-blue-900 pl-4">
                        <p>Title</p>
                        <p class="">$456</p>
                    </div>
                    <div class="border-l-4 border-pink-900 pl-4">
                        <p>Title</p>
                        <p class="">$456</p>
                    </div>
                    <div class="border-l-4 border-yellow-900 pl-4">
                        <p>Title</p>
                        <p class="">$456</p>
                    </div>
                </div>
            </section>
        </main>
    </div>
</template>

<script setup lang="ts">
import NavBar from '@/components/nav/NavBar.vue';
import { WalletIcon } from '@heroicons/vue/16/solid';
</script>