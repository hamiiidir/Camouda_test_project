<template>
  <div>
    <div class="h-auto mb-12" :style="{backgroundImage: backgroundImageStyleUrl, backgroundRepeat: 'repeat-x', backgroundPosition: 'center'}">
      <div class="flex flex-col lg:flex-row items-center lg:items-stretch text-base relative mb-1 lg:mb-28 bg-gray-50 bg-opacity-50">
        <div class="flex justify-around items-center w-full lg:w-auto">
          <img class="w-48" src="../../assets/house-logo.png">
          <div @click="showMainMenu()" class="flex lg:hidden p-2 text-gray-700 bg-pink-600 bg-opacity-50 rounded cursor-pointer">
            <svg class="flex-shrink-0 h-6 fill-current" viewBox="0 0 512 512"><title>Menu</title><path fill="none" stroke="currentColor" stroke-linecap="round" stroke-miterlimit="10" stroke-width="32" d="M80 160h352M80 256h352M80 352h352"/></svg>
          </div>
        </div>
        <div ref="mainMenu" class="z-10 hidden font-normal lg:font-semibold lg:flex flex-col text-2xl lg:text-base lg:flex-row flex-1 absolute lg:relative w-full bg-pink-900 lg:bg-transparent text-white lg:text-gray-900 min-h-screen lg:min-h-0 transform transition-all scale-x-0 lg:scale-x-100">
          <div class="flex flex-col pt-4 lg:pt-0 lg:flex-row justify-start items-start lg:items-center w-auto lg:w-75/100">
            <a class="ml-6 px-4 lg:px-2 py-1 lg:py-0 mt-2 lg:mt-0 cursor-pointer hover:opacity-70">خرید ویلا</a>
            <a class="ml-6 px-4 lg:px-2 py-1 lg:py-0 mt-2 lg:mt-0 cursor-pointer hover:opacity-70">خرید زمین</a>
            <a class="ml-6 px-4 lg:px-2 py-1 lg:py-0 mt-2 lg:mt-0 cursor-pointer hover:opacity-70">مشاورین املاک</a>

            <div @click="toggleContactUsSubmenu()" class="flex justify-start lg:justify-around w-full lg:w-28 items-center ml-6 mb-32 lg:mb-0 mt-2 lg:mt-0 px-4 lg:px-2 py-1 lg:py-0 cursor-pointer relative">
              <div class="hover:opacity-70 ml-2 lg:ml-0">ارتباط با ما</div>
              <svg ref="chevron" class="flex-shrink-0 h-4 fill-current" viewBox="0 0 512 512"><title>Chevron Down</title><path fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="48" d="M112 184l144 144 144-144"/></svg>
              <div ref="contactUsSubmenu" class="flex flex-col absolute w-full lg:w-40 bg-pink-800 lg:bg-blue-600 text-white top-10 lg:top-8 right-0 px-2 py-1 rounded hidden">
                <a class="mr-1 py-1 hover:opacity-70 border-b">تماس با ما</a>
                <a class="mr-1 py-1 hover:opacity-70 ">ارتباط با ما</a>
              </div>
            </div>
          </div>

          <div class="flex flex-col lg:flex-row justify-start lg:justify-around items-start lg:items-center w-auto mb-20 lg:mb-0 px-6 py-2 lg:py-0 rounded text-2xl lg:text-sm bg-pink-800 lg:bg-transparent lg:w-25/100">
            <div class="flex justify-start items-center mb-12 lg:mb-0">
              <svg class="flex-shrink-0 h-8 lg:h-6 fill-current" viewBox="0 0 512 512"><title>Person Circle</title><path d="M258.9 48C141.92 46.42 46.42 141.92 48 258.9c1.56 112.19 92.91 203.54 205.1 205.1 117 1.6 212.48-93.9 210.88-210.88C462.44 140.91 371.09 49.56 258.9 48zm126.42 327.25a4 4 0 01-6.14-.32 124.27 124.27 0 00-32.35-29.59C321.37 329 289.11 320 256 320s-65.37 9-90.83 25.34a124.24 124.24 0 00-32.35 29.58 4 4 0 01-6.14.32A175.32 175.32 0 0180 259c-1.63-97.31 78.22-178.76 175.57-179S432 158.81 432 256a175.32 175.32 0 01-46.68 119.25z"/><path d="M256 144c-19.72 0-37.55 7.39-50.22 20.82s-19 32-17.57 51.93C191.11 256 221.52 288 256 288s64.83-32 67.79-71.24c1.48-19.74-4.8-38.14-17.68-51.82C293.39 151.44 275.59 144 256 144z"/></svg>
              <div class="flex mr-1">
                <a class="mr-4 lg:mr-1 cursor-pointer hover:underline">ورود</a>
                <div class="mr-4 lg:mr-1 cursor-pointer hover:underline">/</div>
                <a class="mr-4 lg:mr-1 cursor-pointer hover:underline">ثبت نام</a>
              </div>
            </div>
            <a class="py-2 px-4 text-white bg-blue-800 hover:bg-blue-700 cursor-pointer rounded-lg transform transition-all hover:scale-105">
              ثبت آگهی
            </a>
          </div>

          <div class="lg:hidden flex justify-center items-center">
            <div @click="hideMainMenu()" class="py-2 px-20 bg-pink-700 text-white rounded-lg cursor-pointer">بازگشت</div>
          </div>
        </div>
      </div>

      <div class="flex flex-col justify-center items-center py-6 font-black text-lg lg:text-5xl pb-8 lg:pb-32">
        <div class="border p-2 bg-gray-50 bg-opacity-60 border-white">سامانه ملکی شمال کشور</div>
        <div class="border p-2 bg-gray-50 bg-opacity-60 border-white">تخصص ما نوار شمالی کشور است</div>
        <div class="border p-2 bg-gray-50 bg-opacity-60 border-white">هزاران ثبت ملک در کشور</div>
      </div>    
    </div>
    
    <div ref="components">
      <search-bar />
      <which-region />
      <special-sale />
      <introduction-cards />
      <ten-best-amlak />
      <statistics />
      <ten-best-moshaver />
      <other-cities />
      <site-footer />
    </div>

  </div>

</template>

<script lang="ts">
  import { defineComponent, ref } from 'vue';
  import searchBar from './SearchBar.vue';
  import whichRegion from './WhichRegion.vue';
  import specialSale from './SpecialSail.vue';
  import introductionCards from './IntroductionsCards.vue';
  import tenBestAmlak from './TenBestAmlak.vue';
  import statistics from './Statistics.vue';
  import tenBestMoshaver from './TenBestMoshaver.vue';
  import otherCities from './OtherCities.vue';
  import siteFooter from './SiteFooter.vue';

  export default defineComponent({
    components: {
      searchBar,
      whichRegion,
      specialSale,
      introductionCards,
      tenBestAmlak,
      statistics,
      tenBestMoshaver,
      otherCities,
      siteFooter
    },

    setup() {
      const components = ref<HTMLElement>();
      const contactUsSubmenu = ref<HTMLElement>();
      const chevron = ref<HTMLElement>();
      const mainMenu = ref<HTMLElement>();

      const toggleContactUsSubmenu = () => {
        contactUsSubmenu.value?.classList.toggle('hidden');
        chevron.value?.classList.toggle('transform')
        chevron.value?.classList.toggle('rotate-180')

      }

      const stopScroll = () => {
        window.scroll(0, 0);
      }

      const showMainMenu = () => {
        components.value?.classList.add('hidden');
        setTimeout(() => {
          mainMenu.value?.classList.remove('hidden');
          setTimeout(() => {
            mainMenu.value?.classList.remove('scale-x-0');
            mainMenu.value?.classList.add('scale-x-100');
          }, 50);
  
          document.body.classList.add('overflow-y-hidden');
          window.addEventListener('scroll', stopScroll);
        }, 50);
      }

      const hideMainMenu = () => {
        mainMenu.value?.classList.remove('scale-x-100');
        mainMenu.value?.classList.add('scale-x-0');
        setTimeout(() => {
          mainMenu.value?.classList.add('hidden');
          document.body.classList.remove('overflow-y-hidden'); 
          window.removeEventListener('scroll', stopScroll);
          components.value?.classList.remove('hidden');      
        }, 150);

      }

      const backgroundImageStyleUrl = window.matchMedia("(min-width: 1024px)").matches ? `url('../../src/assets/house4.jpg')` : `url('../../src/assets/house4-mobile.jpg')`;

      return {
        contactUsSubmenu,
        components,
        toggleContactUsSubmenu,
        chevron,
        showMainMenu,
        mainMenu,
        hideMainMenu,
        backgroundImageStyleUrl
      }
      
    },
})
</script>

