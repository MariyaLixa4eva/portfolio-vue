<template>
    <div class="project">
        <div class="container">
            <div class="project-text">
                <h2>{{ $t("project.title") }}</h2>
            </div>
            <div class="main">
                <ProjectCard class="card" />
            </div>
        </div>
    </div>
</template>

<script>
import ProjectCard from './ProjectCard.vue';
export default {
    components: { ProjectCard },
    data() {
        return {
            props: {
                cards: [],
            }
        }
    }
}
</script>

<style scoped>
.project {
    width: 100%;
}
.container {
    margin: 0 auto;
    max-width: 1200px;
    padding: 20px;
}
.main {
    width: 100%;
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    grid-gap: 1rem;
    margin: 100px 0;
}
.project-text {
    margin-top: 100px;
}
h2  {
    color: var(--bg);
    position: relative;
    margin-bottom: 50px;
    font-size: 4rem;
    -webkit-text-stroke: 0.3px var(--color);
    text-shadow: 1px 1px 5px var(--color);
}
h2::after  {
    content: '';
    position: absolute;
    width: 90px;
    height: 90px;
    background-color: rgb(25, 32, 57, 0.6);
    border-radius: 5px;
    left: 10px;
    transform: rotate(30deg);
    z-index: -1;
    border: 0.5px solid var(--color);
}
h2::before  {
    content: '';
    position: absolute;
    width: 80px;
    height: 80px;
    background-color: rgb(25, 32, 57, 0.6);
    border-radius: 5px;
    left: 55px;
    z-index: -1;
    transform: rotate(15deg);
    border: 0.5px solid var(--color);
}
@media all and (max-width: 600px) {
    h2  {
        font-size: 2.5rem;
    }
}
</style>