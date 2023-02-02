<template>
  <div>
    <h2>Progetti</h2>
    <div class="container">
      <div class="cards">
        <div class="card" v-for="project in projects">
          <CardProject :info="project" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import axios from "axios";
import CardProject from "./CardProject.vue";

export default {
  name: "ListProjects",
  components: {
    CardProject,
  },
  data() {
    return {
      projects: [],
    };
  },
  created() {
    axios.get("http://localhost:8000/api/projects").then((resp) => {
      this.projects = resp.data;
    });
  },
};
</script>

<style lang="scss" scoped>
.container {
  width: 70%;
  margin-left: auto;
  margin-right: auto;
}
.cards {
  padding-top: 50px;
  display: flex;
  flex-wrap: wrap;
  position: relative;
  padding-bottom: 10px;
  .card {
    width: calc(100% / 6);
    padding: 10px;
  }
}
</style>
