<template>
    <div class="card"
    v-for="card in cards"
    :key="card.id">
        <div class="container-img">
            <img
                :src="card.image"
                alt="portfolio"
            >
        </div>
        <div class="container-btn">
            <button><a :href='card.site' target="_blank">{{ $t("project.btn") }}</a></button>
        </div>
    </div>
</template>
<script>
export default {
    data() {
        return {
            cards: [
                { id: 1, image: require('../assets/img/advocat.png'), site: 'https://filimonov-advokat.ru/' },
                { id: 2, image: require('../assets/img/baza.png'), site: 'https://www.bazaradugatus.ru/' },
                { id: 3, image: require('../assets/img/diz.png'), site: 'https://kate-designer-project.glitch.me/' },
                { id: 4, image: require('../assets/img/fit.png'), site: 'https://befit-project1-mine.glitch.me/' },
                { id: 5, image: require('../assets/img/foto.png'), site: 'https://photographer-website-bootstrap.glitch.me/' },
                { id: 6, image: require('../assets/img/music.png'), site: 'https://music-project-week5-js.glitch.me/' },
                { id: 7, image: require('../assets/img/perm.png'), site: 'https://permanent-julia-project.glitch.me/' },
                { id: 8, image: require('../assets/img/port1.png'), site: 'https://project-portfolio-lixa4evamariya.glitch.me/' },
                { id: 9, image: require('../assets/img/port2.png'), site: 'https://mlikhacheva.ru/' },
                { id: 10, image: require('../assets/img/sto.png'), site: 'https://stoaccord19.ru/' },
                { id: 11, image: require('../assets/img/todo.png'), site: 'https://todo-list-and-emoji.netlify.app/' },
                { id: 12, image: require('../assets/img/trener.png'), site: 'https://sport-ml-js.glitch.me/' },
            
            ]
        }
    }
}
</script>
<style scoped>
.container-img {
    width: 100%;
    height: 80%;
    overflow: hidden;
    border: 3px solid white;
    border-radius: 5px;
    box-shadow: 0 0 5px var(--color), 0 0 20px var(--color);
}
.container-img img {
    width: 100%;
    height: 100%;
    transition: 0.5s;
}
.container-img img:hover {
    transform: scale(1.3);
}
.container-btn {
    display: flex;
    justify-content: center;
}
.container-btn button {
    background-color: var(--bg);
    padding: 10px 30px;
    margin: 13px;
    color: #fff;
    border: none;
    border-radius: 5px;
    box-shadow: 0 0 5px var(--color), 0 0 20px var(--color);
    text-transform: uppercase;
}
</style>