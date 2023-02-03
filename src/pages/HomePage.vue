<template>
  <div>
    <h2>Homepage</h2>
    <ListProjects />
  </div>
</template>

<script>
import ListProjects from "../components/ListProjects.vue";

export default {
  name: "HomePage",
  components: {
    ListProjects,
  },
};
</script>

<style lang="scss" scoped></style>
