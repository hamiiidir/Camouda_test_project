<template>
    <div class="flex justify-center items-center h-full w-full mb-12 lg:mb-16">
        <div class="flex justify-center items-center w-80 lg:w-168 overflow-hidden border border-gray-400 rounded-lg">
            <input class="h-10 lg:h-12 px-4 focus:outline-none w-85/100 lg:w-90/100 border-l" placeholder="جستجوی شهر، محله یا منطقه" type="text">
            <svg class="flex-shrink-0 h-8 lg:h-10 fill-current w-15/100 lg:w-10/100 cursor-pointer" viewBox="0 0 512 512"><title>Search</title><path d="M221.09 64a157.09 157.09 0 10157.09 157.09A157.1 157.1 0 00221.09 64z" fill="none" stroke="currentColor" stroke-miterlimit="10" stroke-width="32"/><path fill="none" stroke="currentColor" stroke-linecap="round" stroke-miterlimit="10" stroke-width="32" d="M338.29 338.29L448 448"/></svg>
        </div>
    </div>
</template>

<script lang="ts">
    import { defineComponent } from 'vue';

    export default defineComponent({
        setup() {
            
        },
    })
</script>
