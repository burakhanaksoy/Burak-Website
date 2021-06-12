<template>
  <div class="container">
    <div class="row">
      <div class="col">
        <HelloWorld msg="Hello 👋 " />
      </div>
    </div>
    <div class="row">
      <div class="col">
        <h3>Tech Stack</h3>
        <bars :techList="technologies" />
      </div>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from "@/components/HelloWorld.vue";
import ProgressBars from "@/components/ProgressBars.vue";

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
        { name: "linux", val: 35, variant: "bad" },
        { name: "Vue", val: 40, variant: "bad" },
        { name: "JS", val: 30, variant: "bad" },
      ],
    };
  },

  mounted() {},
};
</script>
<style scoped>
</style>
