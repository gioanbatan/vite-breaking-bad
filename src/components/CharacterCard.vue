<script>
export default {
    name: "CharacterCard",
}
</script>

<template>
    <div class="ms_card d-flex flex-column">
        <!-- <img :src="" :alt=""> -->
        <div>test</div>
        <div>test</div>
    </div>

</template>

<style lang="scss">
@use "../styles/partials/variables" as *;

.ms_card {
    background-color: $bg-color;
    color: $col-white;

    // DEBUG
    width: 100%;
    height: 200px;
}
</style>