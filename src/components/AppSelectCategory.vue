<script>

export default {
    name: "AppSelectCategory"
}
</script>

<template>
    <div class="container mx-auto">
        <div class="ms_category-container">
            <select id="category">
                <option value="???">Select category</option>
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