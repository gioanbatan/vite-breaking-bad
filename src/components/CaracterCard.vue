<script>
export default {
    name: "CaracterCard",
}
</script>

<template>
    <div class="card d-flex flex-column">
        <div>test</div>
        <div>test</div>
        <div>test</div>
    </div>

</template>

<style lang="scss">
@use "../styles/partials/variables" as *;

.card {
    background-color: $bg-color;
    color: $col-white;

    // DEBUG
    width: 90px;
    height: 200px;
}
</style>