<script>
import axios from "axios";
import { store } from "./store";
import AppSelectCategory from "./components/AppSelectCategory.vue";
import AppResults from "./components/AppResults.vue";
import AppLoader from "./components/AppLoader.vue";

export default {
  components: {
    AppSelectCategory,
    AppResults,
    AppLoader
  },
  data() {
    return {
      store,
      dataIsLoaded: false
    }
  },
  created() {
    this.dataIsLoaded = false;
    axios.get("https://www.breakingbadapi.com/api/characters").then((resp) => {
      this.store.characters = resp.data;
      console.log(this.store.characters, typeof (this.store.characters));
      this.dataIsLoaded = true;
    })
  },
  methods: {
    changeSeries() {
      console.log("this.store.seriesSelected", typeof (this.store.seriesSelected));
      let apiString = "https://www.breakingbadapi.com/api/characters";
      if (this.store.seriesSelected !== "All series") {
        apiString = `${apiString}?category=${this.store.seriesSelected}`
      }
      axios.get(apiString).then((resp) => {
        this.store.characters = resp.data;
      });
      console.log(apiString + "?category=" + this.store.seriesSelected);
      console.log(this.store.characters, typeof (this.store.characters));
    }
  }
}

</script>

<template>
  <img class="ms_b-b-logo" src="./assets/img/logo.png" alt="Br Ba Breaking Bad logo">
  <h1 class="d-inline-block align-middle">Breaking Bad Api</h1>
  <div v-if="!dataIsLoaded">
    <AppLoader />
  </div>
  <div v-else>
    <AppSelectCategory @selectSeries="changeSeries" />
    <AppResults />
  </div>
</template>

<style lang="scss">
@use "./styles/general.scss" as *;
@use "./styles/partials/variables" as *;

.ms_b-b-logo {
  width: 50px;
}
</style>