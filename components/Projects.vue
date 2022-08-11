<template>
  <div id="projects-list">
    <h1>My Projects!!!</h1>
    <div id="my-projects" class="relative w-100">
      <div v-for="project in projects" :key="project.id" class="relative bg-black-10 h-25 mbm w-40">
        <div class="absolute top-2 left-2 right-2 bottom-2 white bg-dark-gray o-80 min-h-2">
          <p class="tc">{{project.title}}</p>
        </div>
        <img class="br-pill w-100" :src=project.cover :alt=project.alttext />
      </div>
    </div>
  </div>
</template>

<script>
import projectData from "~/content/projects/projects.json";

export default {
  name: "Projects.vue",
  data() {
    return {
      projects:projectData,
    };
  },
  methods: {
  }
}
</script>

<style scoped>

</style>
