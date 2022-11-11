<template>
  <div
    class="section bg-[url(/images/jumia_black/bg.png)] w-full flex flex-col items-center"
  >
    <TopBanner />
    <HeaderTag />
    <div class="w-9/12 h-full">
      <BannerItem />
      <ProductContainerAds />
      <Product_Container />
      <FlashSales />
    </div>
  </div>
</template>

<script>
import TopBanner from "./components/TopBanner.vue";
import HeaderTag from "./components/Header/Header.vue";
import BannerItem from "./components/Banner/Banner.vue";
import ProductContainerAds from "./components/Product_Ads/ProductContainerAds.vue";
import Product_Container from "./components/Products_Containers/Product_Container.vue";
import FlashSales from "./components/Flash-Sales/FlashSales-Container.vue";

export default {
  name: "App",
  components: {
    TopBanner,
    HeaderTag,
    BannerItem,
    ProductContainerAds,
    Product_Container,
    FlashSales,
  },
};
</script>

<style scoped>
.section {
  background-position: 50% 120%;
}
</style>
