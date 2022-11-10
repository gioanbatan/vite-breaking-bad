<script>
import axios from "axios";
import { store } from "./store";
import AppSelectCategory from "./components/AppSelectCategory.vue";
import AppResults from "./components/AppResults.vue";

export default {
  components: {
    AppSelectCategory,
    AppResults,
  },
  data() {
    return {
      store
    }
  }
}

</script>

<template>
  <h1>Breaking Bad Api</h1>
  <AppSelectCategory />
  <AppResults />



  <div>
    {{ store.test }}
  </div>

</template>

<style lang="scss">
@use "./styles/general.scss" as *;
@use "./styles/partials/variables" as *;
</style>