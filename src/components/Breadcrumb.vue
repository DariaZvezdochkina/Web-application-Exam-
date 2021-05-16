<template>
  <div>
    <h2>Category page for {{ $route.params.alias }}</h2>
    <ProductPanel :category="$route.params.alias" />
  </div>
</template>

<script>
import axios from "axios";
import ProductPanel from "./ProductPanel";

export default {
  name: 'CategoryPage',
  components: {
    ProductPanel
  },
  mounted() {
    axios
      .get("https://euas.person.ee/categories/")
      .then(response => {
        this.categories = response.data;
      });
  }
}
</script>

<style>
  
</style>