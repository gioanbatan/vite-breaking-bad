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
            <select @change="$emit('selectSeries')" id="category">
                <option selected="selected" value="series[0]">{{ series[0] }}</option>
                <option value="series[1]">{{ series[1] }}</option>
                <option value="series[2]">{{ series[2] }}</option>
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