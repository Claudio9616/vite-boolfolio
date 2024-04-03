<script>
import ProjectsList from './components/projects/ProjectsList.vue'
import AppHeader from './components/AppHeader.vue';
import axios from 'axios';
const endpointProjects = 'http://localhost:8000/api/projects/';
export default {
  name: 'Vite-Boolfolio',
  components: {
    AppHeader, ProjectsList
  },
  data: () => ({ projects: [] }),
  methods: {
    fetchProjects() {
      axios.get(endpointProjects).then(res => {
        console.log(res.data);
        this.projects = res.data;
      })
    }
  },
  created() {
    this.fetchProjects();
  }
}
</script>

<template>
  <AppHeader />
  <ProjectsList :projects="projects" />
</template>
<style></style>