<template>
    <div>Show</div>
    <Link href="/">Main Page</Link>
</template>

<script setup>
import { Link } from "@inertiajs/vue3";

const props = defineProps(["message"]);
</script>

<!-- <script>
import MainLayout from "../../Layouts/MainLayout.vue";

export default {
    layout: MainLayout,
};
</script> -->
