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
      this.store.characters = resp.data;
      console.log(this.store.characters, typeof (this.store.characters));
    })
  }
}

</script>

<template>
  <img class="ms_b-b-logo"
    src="../src/assets/img/kisspng-walter-white-television-show-logo-amc-breaking-bad-5abba541179f29.1929777815222469770968.png"
    alt="Br Ba Breaking Bad logo">
  <h1 class="d-inline-block align-middle">Breaking Bad Api</h1>
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

.ms_b-b-logo {
  width: 50px;
  height: 50px;
}
</style>