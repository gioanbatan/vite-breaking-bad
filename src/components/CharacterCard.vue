<script>
export default {
    name: "CharacterCard",
    props: {
        character: Object
    }
}
</script>

<template>
    <div class="ms_card p-3 d-flex flex-column">
        <img :src="character.img" :alt="character.name">
        <span class="ms_name p-2 text-center">{{ character.name.toUpperCase() }}</span>
        <span class="ms_category p-1 text-center">{{ character.category }}</span>
        <span class="ms_status text-center">{{ character.status }}</span>
    </div>

</template>

<style lang="scss">
@use "../styles/partials/variables" as *;

.ms_card {
    background-color: $bg-color;
    color: $col-white;
    // DEBUG
    width: 100%;
    height: 450px;
    overflow: auto;

    .ms_category {
        font-size: 1.5rem;
        font-weight: 100;
        color: $sec-text;
    }

    .ms_status {
        font-size: 1rem;
        font-weight: 500;
        color: $sec-text;
    }
}
</style>