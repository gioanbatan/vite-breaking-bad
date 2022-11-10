<script>
import CharacterCard from "./CharacterCard.vue";
import { store } from "../store";

export default {
    name: "AppResults",
    components: {
        CharacterCard
    },
    data() {
        return {
            store
        }
    }
}
</script>

<template>
    <div class="container mx-auto">
        <section class="ms_results-container p-5">
            <div class="ms_found-bar p-3">
                Found {{ store.characters.length - 1 }} characters
            </div>

            <div class="container-fluid">
                <div class="row row-cols-5 pt-3 pb-3">
                    <div characterclass=" col">
                        <CharacterCard />
                    </div>
                    <div class="col">
                        <CharacterCard />
                    </div>
                    <div class="col">
                        <CharacterCard />
                    </div>
                    <div class="col">
                        <CharacterCard />
                    </div>
                    <div class="col">
                        <CharacterCard />
                    </div>
                </div>

            </div>
        </section>
    </div>
</template>

<style lang="scss" scoped>
@use "../styles/partials/variables" as *;

.ms_results-container {
    background-color: $col-white;
    font-size: 1rem;
    font-weight: 700;
}

.ms_found-bar {
    background-color: $bar-found;
    width: 100%;
}

.ms_testing {
    background-color: black;
    width: 100%;
    height: 100px;
}
</style>