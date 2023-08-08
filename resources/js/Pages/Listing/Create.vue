<template>
    <form>
        <div>
            <div>
                <label>Beds</label>
                <input type="text" v-model.number="form.beds" />
                {{ form.beds }}
            </div>

            <div>
                <label>Baths</label>
                <input type="text" v-model.number="form.baths" />
            </div>

            <div>
                <label>Area</label>
                <input type="text" v-model.number="form.area" />
            </div>

            <div>
                <label>City</label>
                <input type="text" v-model="form.city" />
            </div>

            <div>
                <label>Post Code</label>
                <input type="text" v.model="form.code" />
            </div>

            <div>
                <label>Street</label>
                <input type="text" v.model="form.street" />
            </div>

            <div>
                <label>Street Nr</label>
                <input type="text" v-model.number="form.street_nr" />
            </div>

            <div>
                <label>Price</label>
                <input type="text" v-model="form.price" />
            </div>

            <div>
                <button type="submit">Create</button>
            </div>
        </div>
    </form>
</template>

<style scoped>
label {
    margin-right: 2em;
}

div {
    padding: 2px;
}
</style>

<script setup>
import { reactive } from "vue";
import { Inertia } from "@inertiajs/vue3";

const form = reactive({
    beds: 0,
    baths: 0,
    area: 0,
    city: null,
    code: null,
    street: null,
    street_nr: 0,
    price: 0,
});
</script>
