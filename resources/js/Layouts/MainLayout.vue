<template>
    <Link href="/">Main Page</Link>
    <Link href="/hello">Show Page</Link>
    <!-- <div v-if="page.props.value.flash.success" class="success">Test</div> -->
    <div>The page with time {{ timer }}</div>

    <slot></slot>
</template>

<script setup>
import { Link, usePage } from "@inertiajs/vue3";
import { ref } from "vue";

const timer = ref(0);

const page = usePage();

setInterval(() => timer.value++, 1000);
</script>

<style scoped>
.success {
    background-color: green;
    color: white;
}
</style>
