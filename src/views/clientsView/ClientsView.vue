<script setup>
import Typography from "@/components/UI/Typography.vue";
import { Swiper, SwiperSlide } from "swiper/vue";
import { Autoplay } from "swiper/modules";
import useFetch from "@/services/api";

const { data, isFetching, fetchData } = useFetch();

fetchData("common/partner/list/");

// Import Swiper styles
import "swiper/css";

const modules = [Autoplay];

const breakpoints = {
  320: {
    slidesPerView: 2.5,
  },
  850: {
    slidesPerView: 5.5,
  },
};
</script>

<template>
  <section class="clients">
    <div class="container">
      <Typography class="clients__title title" tagName="h2">Среди наших клиентов</Typography>
      <div class="clients__carousel">
        <Swiper
          class="clients__carousel-slider"
          :modules="modules"
          :spaceBetween="16"
          :breakpoints="breakpoints"
          :speed="2000"
          :loop="true"
          :allowTouchMove="false"
          :autoplay="{
            delay: 0,
          }"
        >
          <SwiperSlide v-for="item in data" :key="item.name">
            <img :src="item.logo" alt="" class="clients__carousel-image" />
          </SwiperSlide>
        </Swiper>
      </div>
    </div>
  </section>
</template>
