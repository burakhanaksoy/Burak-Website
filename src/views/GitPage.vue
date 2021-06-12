<template>
  <div class="page">
    <spinner :isActive="spinnerActive" />
    <h1>Burakhan Aksoy</h1>
    <b-container class="bv-example-row">
      <b-row class="row">
        <div v-for="repo in repos" :key="repo.repo">
          <gitcards
            :repo="repo.repo"
            :description="repo.description"
            :language="repo.language"
            :link="repo.link"
          />
        </div>
      </b-row>
    </b-container>
  </div>
</template>

<script>
import GitCards from "@/components/GitCards.vue";
import Spinner from "@/components/Spinner.vue";
import axios from "axios";

export default {
  name: "GitPage",
  components: {
    gitcards: GitCards,
    spinner: Spinner,
  },
  data: function () {
    return {
      //   repo: "",
      //   description: "",
      //   stars: "",
      //   link: "",
      repos: [],
      spinnerActive: false,
    };
  },
  methods: {
    fetchData: async function () {
      // Axios fetching here!

      axios
        .get(
          "https://gh-pinned-repos-5l2i19um3.vercel.app/?username=burakhanaksoy"
        )
        .then((values) => {
          //   console.log(response.data[0].repo);
          //   this.repo = response.data.repo;
          //   this.description = response.data.description;
          //   this.stars = response.data.stars;
          //   this.link = response.data.link;
          values.data.forEach((data) => {
            this.repos.push(data);
            this.hideSpinner();
          });
        })
        .catch(console.error);
    },

    showSpinner: function () {
      this.spinnerActive = true;
    },
    hideSpinner: function () {
      this.spinnerActive = false;
    },
  },

  created: function () {
    this.showSpinner();
    setTimeout(() => {
      this.fetchData();
    }, 500);
  },
};
</script>

<style scoped>
</style>
