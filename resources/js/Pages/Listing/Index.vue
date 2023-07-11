<script setup>
defineProps({
    listings: Array,
});
</script>

<template>
    <div>Hello!</div>
    <div v-for="listing in listings">
        {{ listing.city }}
    </div>
</template>
