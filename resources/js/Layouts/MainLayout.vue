<template>
    <Link href="/">Main Page</Link>
    <Link href="/hello">Show Page</Link>
    <div v-if="flashSuccess" class="success">
        {{ flashSuccess }}
    </div>
    <div>
        {{ y }}
    </div>
    <div>The page with time {{ timer }}</div>

    <slot></slot>
</template>

<script setup>
import { computed, ref } from "vue";
import { Link, usePage } from "@inertiajs/vue3";

const timer = ref(0);

const x = ref(2);
const y = computed(() => {
    return x.value * 2;
});

const page = usePage();
const flashSuccess = computed(() => {
    return page.props.flash.success;
});

setInterval(() => timer.value++, 1000);
</script>

<style scoped>
.success {
    background-color: green;
    color: white;
}
</style>
