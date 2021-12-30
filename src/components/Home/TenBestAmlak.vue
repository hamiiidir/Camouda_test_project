<template>
    <div dir="ltr" class="px-8 lg:px-20 mb-24 lg:mb-32" style="font-family: normal">
        <div dir="rtl" class="flex justify-center items-center font-semibold text-base lg:text-2xl mb-2">
            <div>10 املاک برتر سراسر شمال</div>
        </div>
        <carousel :settings="settings" :breakpoints="breakpoints" class="mb-24 lg:mb-32">
            <slide class="flex justify-center items-center py-4" v-for="slide in 10" :key="slide">
                <div class="flex flex-col hover:scale-110 transform transition-all">
                    <div class="flex justify-center items-center rounded-full mb-2 w-40 h-40 overflow-hidden border border-pink-300 cursor-pointer">
                        <img src="../../assets/house-logo-square.png" alt="">
                    </div>
                    <div class="cursor-pointer text-base">املاک نمونه</div>
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
            itemsToShow: 1.5,
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
                itemsToShow: 7,
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





