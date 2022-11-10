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
  },
  created() {
    axios.get("https://www.breakingbadapi.com/api/characters").then((resp) => {
      this.store.character = resp.data;
      console.log(this.store.character, typeof (this.store.character));
    })
  }
}

</script>

<template>
  <h1>Breaking Bad Api</h1>
  <AppSelectCategory />
  <AppResults />

  <!-- DEBUG -->
  <div>
    {{ store.test }}
  </div>

</template>

<style lang="scss">
@use "./styles/general.scss" as *;
@use "./styles/partials/variables" as *;
</style>