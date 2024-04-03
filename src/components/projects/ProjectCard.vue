<script>
export default {
    name: 'ProjectCard',
    props: {
        project: Object
    }
}
</script>

<template>
    <div class="container">
        <div class="card">
            <div class="card-body">
                <h2 class="card-title">{{ project.title }}</h2>
                <p class="card-text">{{ project.description }}</p>

            </div>
        </div>
    </div>
</template>
<style></style>