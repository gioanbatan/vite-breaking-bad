<script>
import CaracterCard from "./CaracterCard.vue";
export default {
    name: "AppResults",
    components: {
        CaracterCard
    }
}

</script>

<template>
    <div class="container">
        <section class="results-container">
            <div class="found-bar">
                Found xx chatacters
            </div>

            <div class="row row-cols-5">
                <div class="col">
                    <CaracterCard />
                </div>
                <div class="col">
                    <CaracterCard />
                </div>
                <div class="col">
                    <CaracterCard />
                </div>
            </div>
        </section>
    </div>
</template>

<style lang="scss" scoped>
@use "../styles/partials/variables" as *;

.results-container {
    background-color: $col-white;
    padding: 3rem;
    font-size: 1rem;
    font-weight: 700;
}

.found-bar {
    background-color: $bar-found;
    padding: 1rem;
}
</style>