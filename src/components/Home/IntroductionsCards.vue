<template>
    <div class="flex flex-col justify-center items-center w-full font-semibold px-8 lg:px-20 mb-24 lg:mb-32" >
        <div class="grid grid-row-3 lg:grid-cols-3 gap-4">
            <div class="flex justify-center items-center text-xl rounded-lg overflow-hidden relative">
                <img src="../../assets/introduction-cards/house-and-key.jpg" alt="">
                <div class="absolute bottom-0 left-0 right-0 bg-gray-50 bg-opacity-70 p-4">
                    <div>مالک هستید؟</div>
                    <div class="mb-7">ملکتان را در سریع ترین زمان به فروش برسانید.</div>
                </div>
            </div>
            <div class="flex justify-center items-center text-xl rounded-lg overflow-hidden relative">
                <img src="../../assets/introduction-cards/buyer-satisfaction.jpg" alt="">
                <div class="absolute bottom-0 left-0 right-0 bg-gray-50 bg-opacity-70 p-4">
                    <div>خریدار هستید؟</div>
                    <div>در سریع ترین زمان و به راحتی ملکی که دنبالش هستید را پیدا کنید و بخرید.</div>
                </div>
            </div>
            <div class="flex justify-center items-center text-xl rounded-lg overflow-hidden relative">
                <img src="../../assets/introduction-cards/man-on-telephone.jpg" alt="">
                <div class="absolute bottom-0 left-0 right-0 bg-gray-50 bg-opacity-70 p-4">
                    <div>مشاور املاک هستید؟</div>
                    <div>با یک کلیک در کوتاهترن زمان برای خودتان پنل شخصی داشته باشد.</div>
                </div>
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
