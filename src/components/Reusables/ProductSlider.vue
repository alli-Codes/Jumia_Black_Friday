<template>
    <div class="
     h-80 w-full flex flex-col">
        <swiper :slidesPerView="6" :spaceBetween="10" :navigation="true" :modules="modules"
            class=" product__section flex-1 w-full mySwiper p-4">
            <swiper-slide class="bg-transparent" v-for="item in productData">
                <Products :description="item.description" :price="item.price" :formerPrice="item.formerPrice"
                    :image="item.image" :key="item.index" :progressVisibility="progressVisibility" />
            </swiper-slide>

        </swiper>
    </div>
</template>

<script>
import Products from './Products.vue'

import { Swiper, SwiperSlide } from "swiper/vue";
import "swiper/css";
import "swiper/css/pagination";
import "swiper/css/navigation";
// import "./product.css";
import { Pagination, Navigation } from "swiper";

export default {
    name: 'Product-Container',
    components: {
        Products,
        Swiper,
        SwiperSlide,
    },
    props: {
        productData: Array,
        progressVisibility: Boolean
    },
    setup() {
        return {
            modules: [Pagination, Navigation],
        };
    },
}
</script>