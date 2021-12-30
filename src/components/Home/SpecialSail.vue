<template>
    <div class="flex flex-col justify-center items-center w-full px-8 lg:px-20 mb-24 lg:mb-32">
        <div class="text-base lg:text-2xl mb-4 font-semibold">فروش ویژه هفته</div>
        <div class="grid grid-row-3 lg:grid-cols-3 gap-4">
            <div class="flex flex-col justify-center items-center p-2 border rounded-lg shadow">
                <div class="mb-6 h-full w-full rounded overflow-hidden">
                    <img class="transform transition-all duration-300 hover:scale-125 cursor-pointer" src="../../assets/apartments/apartment1.jpg" alt="">
                </div>
                <div class="mb-2 px-10 py-2 border rounded-lg hover:bg-blue-100 cursor-pointer">اطلاعات ملک</div>
            </div>
            <div class="flex flex-col justify-center items-center p-2 border rounded-lg shadow">
                <div class="mb-6 h-full w-full rounded overflow-hidden">
                    <img class="transform transition-all duration-300 hover:scale-125 cursor-pointer" src="../../assets/apartments/apartment2.jpg" alt="">
                </div>
                <div class="mb-2 px-10 py-2 border rounded-lg hover:bg-blue-100 cursor-pointer">اطلاعات ملک</div>
            </div>
            <div class="flex flex-col justify-center items-center p-2 border rounded-lg shadow">
                <div class="mb-6 h-full w-full rounded overflow-hidden">
                    <img class="transform transition-all duration-300 hover:scale-125 cursor-pointer" src="../../assets/apartments/apartment3.jpg" alt="">
                </div>
                <div class="mb-2 px-10 py-2 border rounded-lg hover:bg-blue-100 cursor-pointer">اطلاعات ملک</div>
            </div>
        </div>
    </div>
</template>

<script lang="ts">
    import { defineComponent } from 'vue'

    export default defineComponent({
        setup() {
            
        }
    })
</script>
