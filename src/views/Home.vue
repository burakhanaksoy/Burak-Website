<template>
  <div class="container">
    <div class="row">
      <div class="col">
        <HelloWorld />
        <!-- <p>{{ $t("message") }} 👋</p> -->
      </div>
    </div>
    <div class="row">
      <div class="col">
        <h3>{{ techStack }}</h3>
        <bars :techList="technologies" />
      </div>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from "@/components/HelloWorld.vue";
import ProgressBars from "@/components/ProgressBars.vue";
import { mapState } from "vuex";

export default {
  name: "Home",
  components: {
    HelloWorld,
    bars: ProgressBars,
  },
  data: function () {
    return {
      technologies: [
        { name: "Python", val: 60, variant: "good" },
        { name: "CSS", val: 40, variant: "mid" },
        { name: "HTML", val: 70, variant: "good" },
        { name: "Mongodb", val: 50, variant: "mid" },
        { name: "Linux", val: 35, variant: "bad" },
        { name: "Vue", val: 40, variant: "bad" },
        { name: "JS", val: 30, variant: "bad" },
      ],
      techStack: this.$t("techStack"),
    };
  },
  computed: {
    ...mapState({
      lang: "language",
    }),
  },

  watch: {
    lang: function (val) {
      if (val) {
        this.changeView(val);
        this.techStack = this.$t("techStack");
      }
    },
  },

  methods: {
    changeView: function (val) {
      this.$i18n.locale = val;
      this.home = this.$t("home");
      this.about = this.$t("about");
      this.github = this.$t("github");
    },
  },
};
</script>
<style scoped></style>
