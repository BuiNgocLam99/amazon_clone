<script setup>
import AuthenticatedLayout from '@/Layouts/AuthenticatedLayout.vue';
import { Head, Link } from '@inertiajs/vue3';
import { toRefs } from 'vue';
import MapMarkerOutlineIcon from 'vue-material-design-icons/MapMarkerOutline.vue';
import PlusIcon from 'vue-material-design-icons/Plus.vue';

const props = defineProps({ product: Object });
const { product } = toRefs(props);

let show = true;
</script>

<template>
    <Head title="Address" />

    <AuthenticatedLayout>
        <div class="mt-12"></div>

        <div class="max-w-[1000px] mx-auto text-3xl mb-10">
            Your Address
        </div>

        <div class="max-w-[1000px] mx-auto flex gap-2 h-[270px]">
            <div class="border border-dotted border-gray-400 rounded-md w-1/3">
                <Link v-if="show" href="/">
                    <div class="grid h-full place-items-center cursor-pointer">
                        <div class="text-center">
                            <div class="flex justify-center">
                                <PlusIcon :size="50" />
                            </div>
                            <div class="font-bold text-2xl">Add Address</div>
                        </div>
                    </div>
                </Link>
            </div>
        </div>
    </AuthenticatedLayout>
</template>
