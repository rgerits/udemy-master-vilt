<script setup>
import { Link } from "@inertiajs/vue3";

const props = defineProps({
    message: String,
});
</script>

<!-- <script>
import MainLayout from "../../Layouts/MainLayout.vue";

export default {
    layout: MainLayout,
};
</script> -->

<template>
    <div>Index</div>
    <Link href="/hello">Show Page</Link>
    <div>Message is: {{ message }}</div>
</template>
