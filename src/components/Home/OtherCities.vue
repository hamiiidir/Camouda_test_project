<template>
    <div dir="ltr" class="px-8 lg:px-20 mb-24 lg:mb-32" style="font-family: normal">
        <div dir="rtl" class="flex justify-center items-center font-semibold text-base lg:text-2xl mb-2">
            <div>سایر شهرهای شمال</div>
        </div>
        <carousel :settings="settings" :breakpoints="breakpoints" class="mb-24 lg:mb-32">
            <slide class="h-full rounded shadow-xl py-4" v-for="(city, index) in cities" :key="index">
                <div class="flex flex-col justify-start items-start px-2 hover:scale-105 transition-all">
                    <div class="flex justify-start items-start mb-2 rounded-lg overflow-hidden cursor-pointer">
                        <img :src="city[1]" alt="">
                    </div>
                    <div dir="rtl" class="px-1 text-justify cursor-pointer text-base"> {{ city[2] }} </div>
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

        const cities = [
            ['چالوس', '/src/assets/cities/Chaloos.jpg', 'چالوس از شهرهای کهن استان مازندران است که در جلگه میانی کرانه دریای خزر جای گرفته‌است. شهر چالوس در شرق شهرستان چالوس قرار دارد. اکثریت جمعیت شهر چالوس را بومیان کلارستاق که طبری‌تبار هستند تشکیل می‌دهند. مردم بومی شهر چالوس به لهجه ای از زبان مازندرانی گویش می‌کنند.'],
            ['نور', '/src/assets/cities/Noor.jpg', 'شهرستان نور از شمال به دریای مازندران، از شرق به شهرستان آمل، از شمال شرق به شهرستان محمودآباد از جنوب به استان تهران، از جنوب غرب به استان البرز و از غرب به شهرستان نوشهر و شهرستان چالوس متصل است. مردم شهرستان نور به زبان طبری و با گویش کجوری صحبت می‌کنند.'],
            ['نوشهر', '/src/assets/cities/Noshahr.jpg', 'نوشهر یکی از شهرهای استان مازندران ایران است. جمعیت این شهر بر طبق سرشماری سال ۱۳۹۵، برابر با ۴۹٬۴۰۵ نفر بوده‌است. نوشهر مهمترین شهر غرب استان مازندران می‌باشد. زبان مردم این شهرستان زبان طبری با گویش کجوری است که به گویش مردم شهرستان نور و چالوس شباهت دارد.'],
            ['ساری', '/src/assets/cities/Sari.jpg', 'ساری (دربارهٔ این پرونده تلفظ راهنما·اطلاعات) از پرجمعیت‌ترین شهرهای شمال و پایتخت پیشین ایران، مرکز استان مازندران و شهرستان ساری است. این شهر پرجمعیت‌ترین و بزرگترین شهر استان مازندران و از بزرگترین شهرهای شمال کشور به‌شمار می‌رود. ساری همچنین یکی از قدیمی‌ترین شهرهای ایران محسوب می‌شود.'],
            ['محمودآباد', '/src/assets/cities/Mahmoudabad.jpg', 'محمودآباد نام شهری ساحلی در مجاورت دریای مازندران است. این شهر مرکز شهرستان محمودآباد است. اقتصاد این شهر برپایه گردشگری، ماهیگیری و کشاورزی استوار است.'],
            ['بابلسر', '/src/assets/cities/Babolsar.jpg', 'بابُلْسَر یکی از شهرهای ساحلی استان مازندران، در شمال ایران، بین دریای مازندران و رشته کوه البرز قرار دارد. این شهر مرکز شهرستان بابلسر است. جمعیت بابلسر براساس سرشماری سال ۹۵ معادل ۵۹۹۶۶ نفر می‌باشد. بابلسر با پهنه ۱۳۵۰ هکتار در مصب رودخانه بابلرود و در کرانه جنوبی دریای مازندران و در ۵۲ درجه و ۳۹ دقیقه و ۳۰ ثانیه طول جغرافیایی و ۳۶ درجه و ۴۳ دقیقه عرض جغرافیایی قرار دارد. مردم بابلسر به گویش بابلی گویش می‌کنند.'],
            ['بابل', '/src/assets/cities/Babol.jpg', 'شهرستان بابُل پرجمعیت‌ترین شهرستانِ استان مازندران و دومین شهرستان پرجمعیت شمال ایران و همچنین پرجمعیت‌ترین شهرستان طبری‌نشین جهان می‌باشد. شهرستان بابل دارای ۶ بخش، ۷ شهر و نیز ۶۷۳ روستا می‌باشد. مرکز این شهرستان، شهر بابل است. بابل به مدت یک دهه است که المپیکی‌ترین شهر ایران می‌باشد.'],
            ['آمل', '/src/assets/cities/Amol.jpg', 'شهرستان آمل در مرکز استان مازندران قرار دارد و از شمال به شهرستان محمودآباد، از شمال شرق به شهرستان فریدون‌کنار، از شرق به شهرستان بابل، از غرب به شهرستان نور و از جنوب به استان تهران محدود می‌شود. مرکز این شهرستان شهر آمل است.'],
        ]

        return {
            settings,
            breakpoints,
            cities
        }
    }

});
</script>





