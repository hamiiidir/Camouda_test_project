<template>
    <div dir="ltr" class="px-8 lg:px-20 mb-24 mb-24 lg:mb-32" style="font-family: normal">
        <div dir="rtl" class="flex justify-center items-center font-semibold text-base lg:text-2xl mb-2">
            <div>10 مشاور برتر سراسر شمال</div>
        </div>
        <carousel :settings="settings" :breakpoints="breakpoints" class="mb-24 lg:mb-32">
            <slide class="flex justify-center items-center py-4" v-for="slide in 10" :key="slide">
                <div class="flex flex-col w-72 p-2 border rounded-lg">
                    <div dir="rtl" class="flex justify-start items-center px-1 mb-6">
                        <div class="flex order-1 justify-center items-center rounded-full mb-2 ml-2 w-28 h-28 overflow-hidden border border-pink-300">
                            <img src="../../assets/house-logo-square.png" alt="">
                        </div>
                        <div dir="rtl" class="flex flex-col justify-start items-start order-2">
                            <div class="mb-3">نام و نام خانوادگی</div>
                            <div>نام املاک</div>
                        </div>
                    </div>
                    <div class="w-full px-6">
                        <div class="cursor-pointer text-base border py-2 rounded-lg mb-4 hover:bg-blue-100 hover:scale-105 transition-all">مشاهده پروفایل</div>
                    </div>
                </div>
            </slide>

            <template #addons>
                <navigation />
                <pagination />
            </template>
        </carousel>
    </div>   
</template>

<script>
import { defineComponent } from 'vue';
import { Carousel, Navigation, Pagination, Slide } from 'vue3-carousel';

export default defineComponent({
    name: 'Breakpoints',
    components: {
        Carousel,
        Slide,
        Pagination,
        Navigation,
    },

    setup(props) {
        const settings = {
            itemsToShow: 1,
            snapAlign: 'center',
        }

        const breakpoints = {
            // 700px and up
            700: {
                itemsToShow: 3.5,
                snapAlign: 'center',
            },
            // 1024 and up
            1024: {
                itemsToShow: 4,
                snapAlign: 'start',
            },
        }

        return {
            settings,
            breakpoints,
        }
    }

});
</script>





