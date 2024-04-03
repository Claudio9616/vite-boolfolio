<script>
import ProjectCard from './ProjectCard.vue';

export default {
    name: 'ProjectsList',
    props: {
        projects: Array
    },
    components: {
        ProjectCard
    }
}
</script>

<template>
    <div class="container">
        <ProjectCard v-for="project in projects" :key="project.id" :project="project" />
    </div>
</template>
<style></style>