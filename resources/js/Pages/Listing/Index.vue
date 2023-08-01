<script setup>
import { Link } from "@inertiajs/vue3";
defineProps({
    listings: Array,
});
</script>

<template>
    <div>Hello!</div>
    <div v-for="listing in listings" :key="listing.id">
        {{ listing.street }}, {{ listing.street_nr }}, {{ listing.city }}, for
        ${{ listing.price }}
    </div>
</template>
