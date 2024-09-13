<template>
    <header class="bg-slate-200 p-6 sticky z-10">
        <nav class="container mx-auto flex justify-between items-center">
            <div class="font-mono font-bold uppercase">Aloha Tiger</div>
            <ul class="flex space-x-6">
                <li>
                    <NuxtLink
                        class="text-gray-800 hover:text-blue-500 uppercase text-sm font-medium"
                        to="/"
                        >Home</NuxtLink
                    >
                </li>
                <li>
                    <NuxtLink
                        class="text-gray-800 hover:text-blue-500 uppercase text-sm font-medium"
                        to="/about"
                        >About</NuxtLink
                    >
                </li>
                <li>
                    <NuxtLink
                        class="text-gray-800 hover:text-blue-500 uppercase text-sm font-medium"
                        to="/cases"
                        >Cases</NuxtLink
                    >
                </li>
                <li>
                    <NuxtLink
                        class="text-gray-800 hover:text-blue-500 uppercase text-sm font-medium"
                        to="/toggle"
                        >Toggle</NuxtLink
                    >
                </li>
                <li>
                    <NuxtLink
                        class="text-gray-800 hover:text-blue-500 uppercase text-sm font-medium"
                        to="/contact"
                        >Contact</NuxtLink
                    >
                </li>
            </ul>
        </nav>
    </header>
</template>

<script lang="ts" setup></script>
