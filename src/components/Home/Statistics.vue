<template>
    <div dir="rtl" class="text-2xl lg:text-3xl px-8 lg:px-20 mb-24 lg:mb-32">
        <div class="grid grid-row-3 lg:grid-cols-3 gap-4">
            <div class="flex flex-col justify-center items-center w-full h-32 lg:h-44 shadow-xl bg-emerald-300 border rounded border-2 border-emerald-500">
                <div class="flex justify-center items-center w-full mb-4">
                    <div class="ml-4 font-semibold"> {{ numberSeparator(125000, ",") }} </div>
                    <!-- <div>عدد</div> -->
                </div>
                <div>ملک آگهی شده در (اسم سایت)</div>
            </div>

            <div class="flex flex-col justify-center items-center w-full h-32 lg:h-44 shadow-xl bg-indigo-300 border rounded border-2 border-indigo-500">
                <div class="flex justify-center items-center w-full mb-4">
                    <div class="ml-4 font-semibold"> {{ numberSeparator(96000, ",") }} </div>
                    <!-- <div>عدد</div> -->
                </div>
                <div>مشاورین فعال در سراسر شمال</div>
            </div>

            <div class="flex flex-col justify-center items-center w-full h-32 lg:h-44 shadow-xl bg-rose-300 border rounded border-2 border-rose-500">
                <div class="flex justify-center items-center w-full mb-4">
                    <div class="ml-4 font-semibold"> {{ numberSeparator(423000, ",") }} </div>
                    <!-- <div>عدد</div> -->
                </div>
                <div>بازدید هفتگی در (اسم سایت)</div>
            </div>
        </div>
    </div>    
</template>

<script>
import { defineComponent } from 'vue';
import numberSeparator from "number-separator";

export default defineComponent({
    setup() {
        return {
            numberSeparator
        }
    },
})
</script>
