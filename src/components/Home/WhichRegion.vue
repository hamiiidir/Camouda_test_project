<template>
    <div class="flex flex-col justify-center items-center mb-12 lg:mb-16">
        <div class="text-base lg:text-2xl mb-4">کدام منطقه یا ملک را می خواهید؟</div>
        <div class="flex flex-col justify-center items-center w-80/100 lg:w-40/100">
            <a class="py-2 lg:py-2 w-full text-center border rounded-lg shadow cursor-pointer hover:bg-blue-100 mb-2">همه ملکهای شمال</a>
            <div class="grid grid-cols-2 gap-2 w-full">
                <div class="border px-2 py-2 text-center rounded-lg shadow cursor-pointer hover:bg-blue-100">چمستان</div>
                <div class="border px-2 py-2 text-center rounded-lg shadow cursor-pointer hover:bg-blue-100">ایزدشهر</div>
                <div class="border px-2 py-2 text-center rounded-lg shadow cursor-pointer hover:bg-blue-100">نوشهر</div>
                <div class="border px-2 py-2 text-center rounded-lg shadow cursor-pointer hover:bg-blue-100">آمل</div>
                <div class="border px-2 py-2 text-center rounded-lg shadow cursor-pointer hover:bg-blue-100">نور</div>
                <div class="border px-2 py-2 text-center rounded-lg shadow cursor-pointer hover:bg-blue-100">رویال</div>
                <div class="border px-2 py-2 text-center rounded-lg shadow cursor-pointer hover:bg-blue-100">چالوس</div>
                <div class="border px-2 py-2 text-center rounded-lg shadow cursor-pointer hover:bg-blue-100">محمود آباد</div>
            </div>
        </div>
    </div>
</template>

<script lang="ts">
    import { defineComponent } from 'vue'

    export default defineComponent({
        setup() {
            
        },
    })
</script>
