<script setup>
import LinkSection from '@/Components/LinkSection.vue';
import { Link } from '@inertiajs/vue3';

defineProps({
    isCollapsed: Boolean
})
</script>

<template>
    <nav>
        <Link href="/dashboard" class="flex items-center space-x-2">
            <img src="https://cdn2.vectorstock.com/i/1000x1000/60/06/letter-a-logo-vector-25576006.jpg" alt="" class="w-[30px] rounded-sm">
            <span v-show="!isCollapsed" class="text-2xl text-white font-extrabold">Ace Joy Villarmia</span>
        </Link>
        <hr class="mt-4">

        <span v-show="!isCollapsed" class="text-[10px] uppercase font-bold text-gray-300 select-none">Navigation</span>

        <LinkSection :isCollapsed="isCollapsed" />
    </nav>
</template>
