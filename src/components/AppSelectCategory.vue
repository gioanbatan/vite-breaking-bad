<script>

export default {
    name: "AppSelectCategory"
}
</script>

<template>
    <div class="container margin-auto">
        <div class="category-container">
            <select id="category">
                <option value="???">Select category</option>
            </select>
        </div>
    </div>
</template>

<style lang="scss" scoped>
.category-container {
    padding: 1rem;

    select {
        padding: 0.4rem
    }
}
</style>