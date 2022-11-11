<script>
import { store } from "../store";

export default {
    name: "AppSelectCategory",
    data() {
        return {
            store,
            series: ['All series', 'Breaking Bad', 'Better Call Saul']
        }
    }
}
</script>

<template>
    <div class="container mx-auto">
        <div class="ms_category-container">
            <select @change="$emit('selectSeries')" id="category" v-model="store.seriesSelected">
                <option selected value="" disabled hidden>Select category</option>
                <option v-for="(selectedCategory, index) in series" :value="selectedCategory" :key="index">{{
                        selectedCategory
                }}</option>
            </select>
        </div>
    </div>
</template>

<style lang="scss" scoped>
.ms_category-container {
    padding: 1rem;

    select {
        padding: 0.4rem
    }
}
</style>