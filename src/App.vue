<template>
  <div id="app">
    <h2>Example</h2>
    <div class="col-md-4" style="width: 350px; margin:auto;">
    <VSelect
      v-model="selected"
      :options="countries"
      :disabled="disabled"
      :searchable="searchable"
      search-placeholder="Search Bar"
      search-not-found="Record Not Found"
      default-title="Select Country"
    />
    </div>
  </div>
</template>

<script>
import VSelect from "@/vue-select-picker-bootstrap";
export default {
  name: "App",
  components: {
    VSelect
  },
  data() {
    return {
      countries: [
        { value: 1, text: "Pakistan" },
        { value: 2, text: "China" },
        { value: 3, text: "Bangladesh" },
        { value: 4, text: "USA" },
        { value: 5, text: "Australia" },
      ],
      disabled:false,
      searchable:true,
      selected: {value: null},
    };
  }
};
</script>
<style>
@import 'https://pro.fontawesome.com/releases/v5.10.0/css/all.css';
</style>
<style lang="scss" scoped>
#app {
  font-family: "Roboto", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  padding: 2em 1em;
}

.options {
  text-align: left;
  padding: 1em 0em;
}
</style>
