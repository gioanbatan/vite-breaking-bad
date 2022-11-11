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
                Found {{ store.characters.length }} characters
            </div>

            <div class="container-fluid">
                <div class="row row-cols-2 row-cols-md-3 row-cols-lg-5 pt-3 g-3">
                    <div v-for="character in store.characters" :key="character.char_id"
                        class="col flex-align-items-stretch">
                        <CharacterCard :character="character" />
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