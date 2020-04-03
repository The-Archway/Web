<template>
  <b-container>
    <b-navbar toggleable type="dark" variant="light">
      <b-nav-form inline @submit="search">
        <b-form-input size="sm" class="mr-sm-2" placeholder="Symbol" v-model="searchText"></b-form-input>
        <b-button size="sm" class="my-2 my-sm-0" @click="search">Search</b-button>
      </b-nav-form>
      <b-spinner label="Loading..." v-if="searching"></b-spinner>
      <b-nav-form inline v-if="fields.length > 0">
        <b-form-select
          style="width: 100%;"
          v-model="selected"
          :options="fields"
          multiple
          :select-size="4"
        ></b-form-select>
      </b-nav-form>
    </b-navbar>
    <b-table striped hover :items="financials" :fields="selected"></b-table>
  </b-container>
</template>

<script>
import axios from "axios";
export default {
  data() {
    return {
      fields: [],
      financials: [],
      searching: false,
      searchText: "",
      selected: []
    };
  },
  methods: {
    search: function(e) {
      this.fields = [];
      this.searching = true;
      const url = `https://vueserver-bkplaamqqa-ue.a.run.app/?symbol=${this.searchText}`;
      axios
        .get(url)
        .then(response => {
          this.financials = response.data;
          if (this.financials.length > 0) {
            this.fields = Object.keys(this.financials[0]);
          }
          this.searching = false;
        })
        .catch(error => {
          console.log(error);
          this.searching = false;
        });

        e.preventDefault();
    }
  }
};
</script>

<style lang="scss" scoped>
</style>