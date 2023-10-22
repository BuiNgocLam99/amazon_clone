<script setup>
import AuthenticatedLayout from '@/Layouts/AuthenticatedLayout.vue';
import { Head } from '@inertiajs/vue3';

import 'vue3-carousel/dist/carousel.css'
import { Carousel, Navigation, Slide } from 'vue3-carousel'
</script>

<template>
    <Head title="Dashboard" />

    <AuthenticatedLayout>
        <Carousel :items-to-show="1" :wrap-around="true">
            <Slide v-for="slide in 10" :key="slide">
                <div class="carousel__item">
                    <img src="https://via.placeholder.com/1500x350.png/004466?text=Testing" alt="">
                </div>
            </Slide>

            <template #addons>
                <Navigation />
            </template>
        </Carousel>
    </AuthenticatedLayout>
</template>

<style>
    .carousel__item {
        font-size: 20-px;
        display: flex;
        justify-content: center;
        align-items: center;
    }

    .carousel__prev,
    .carousel__next {
        width: 40px;
        height: 200px;
        color: rgb(196, 196, 196);
        margin-top: -100px;
        border: transparent;
    }

    .carousel__prev:hover,
    .carousel__next:hover {
        width: 40px;
        height: 200px;
        color: rgb(212, 212, 212);
        margin-top: -100px;
        border: 3px solid rgb(217, 217, 217);
    }
</style>
