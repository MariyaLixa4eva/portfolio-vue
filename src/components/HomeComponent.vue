<template>
<div class="home">
    <div class="container">
        <p>{{ $t("home.hello") }}</p>
        <h1>{{ $t("home.welcome") }}</h1>
        <button>
            <span></span>
            <span></span>
            <span></span>
            <span></span>
            <router-link to="/project">{{ $t("home.button") }}</router-link>
        </button>
    </div>
</div>
</template>




<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Bebas+Neue&family=Open+Sans&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Comfortaa:wght@700&display=swap');
.home {
    width: 100%;
    height: 100dvh;
    position: relative;
    display: flex;
    align-items: center;
    font-family: 'Comfortaa', cursive;
}
.container {
    margin: 0 auto;
    max-width: 1200px;
    padding: 20px;
}
p {
    color: #767990;
    font-size: 2rem;
    margin-bottom: 20px;
}
h1 {
    color: white;
    font-size: 6rem;
}
h1::before {
    content: 'DEVELOPER';
    font-size: 21rem;
    color: #192039;
    position: absolute;
    z-index: -1;
    transform: rotate(-15deg);
    top: 20%;
    font-family: 'Bebas Neue', cursive;
}
h1::after {
    content: '\25A0';
    font-size: 3rem;
    color: var(--color);
    position: relative;
    left: 5px;
}
button {
    position: relative;
    padding: 15px 30px;
    color: var(--color);
    font-size: 1.8rem;
    text-transform: uppercase;
    overflow: hidden;
    transition: .5s;
    margin-top: 40px;
    letter-spacing: 4px;
    background-color: transparent;
    border-radius: 5px;
    border: none;
}
button:hover {
    background: var(--color);
    color: #fff;
    border-radius: 5px;
    box-shadow: 0 0 5px var(--color),
                0 0 25px var(--color),
                0 0 50px var(--color),
                0 0 100px var(--color);
}
button a:hover {
    color: #fff;
}
button span {
    position: absolute;
    display: block;
}
button span:nth-child(1) {
    top: 0;
    left: -100%;
    width: 100%;
    height: 3px;
    background: linear-gradient(90deg, transparent, var(--color));
    animation: btn-anim1 1s linear infinite;
}
@keyframes btn-anim1 {
    0% {
        left: -100%;
    }
    50%,100% {
        left: 100%;
    }
}
button span:nth-child(2) {
    top: -100%;
    right: 0;
    width: 3px;
    height: 100%;
    background: linear-gradient(180deg, transparent, var(--color));
    animation: btn-anim2 1s linear infinite;
    animation-delay: .25s
}
@keyframes btn-anim2 {
    0% {
        top: -100%;
    }
    50%,100% {
        top: 100%;
    }
}
button span:nth-child(3) {
    bottom: 0;
    right: -100%;
    width: 100%;
    height: 3px;
    background: linear-gradient(270deg, transparent, var(--color));
    animation: btn-anim3 1s linear infinite;
    animation-delay: .5s
}
@keyframes btn-anim3 {
    0% {
        right: -100%;
    }
    50%,100% {
        right: 100%;
    }
}
button span:nth-child(4) {
    bottom: -100%;
    left: 0;
    width: 3px;
    height: 100%;
    background: linear-gradient(360deg, transparent, var(--color));
    animation: btn-anim4 1s linear infinite;
    animation-delay: .75s
}
@keyframes btn-anim4 {
    0% {
        bottom: -100%;
    }
    50%,100% {
        bottom: 100%;
    }
}
@media all and (max-width: 1190px) {
    h1 {
        font-size: 4rem;
    }
    h1::before {
    content: 'DEVELOPER';
    font-size: 21rem;
    color: #192039;
    position: absolute;
    z-index: -1;
    transform: rotate(-90deg);
    top: 37%;
    left: 200px;
    font-family: 'Bebas Neue', cursive;
}
button {
    font-size: 2rem;
}
}
@media all and (max-width: 900px) {
    h1 {
        font-size: 4rem;
    }
    h1::before {
    content: 'DEVELOPER';
    font-size: 18rem;
    color: #192039;
    position: absolute;
    z-index: -1;
    transform: rotate(-90deg);
    top: 40%;
    left: 200px;
    font-family: 'Bebas Neue', cursive;
}
h1::after {
    content: '\25A0';
    font-size: 2.5rem;
    color: var(--color);
    position: relative;
    left: 5px;
}
button {
    font-size: 2rem;
}
}
@media all and (max-width: 600px) {
    h1 {
        font-size: 2.5rem;
    }
    h1::before {
    content: 'DEVELOPER';
    font-size: 10rem;
    color: #192039;
    position: absolute;
    z-index: -1;
    transform: rotate(-90deg);
    top: 40%;
    left: 200px;
    font-family: 'Bebas Neue', cursive;
}
h1::after {
    content: '\25A0';
    font-size: 2.5rem;
    color: var(--color);
    position: relative;
    left: 5px;
}
button {
    font-size: 1rem;
}
}
@media all and (max-width: 580px) {
    /* .container {
    margin: 0 auto;
    max-width: 1200px;
    padding: 20px;
} */
    h1 {
        font-size: 1.8rem;
    }
    h1::before {
    content: 'DEVELOPER';
    font-size: 10rem;
    color: #192039;
    position: absolute;
    z-index: -1;
    transform: rotate(-90deg);
    top: 40%;
    left: -10px;
    font-family: 'Bebas Neue', cursive;
}
h1::after {
    content: '\25A0';
    font-size: 2.5rem;
    color: var(--color);
    position: relative;
    left: 5px;
}
button {
    font-size: 1rem;
}
}
</style>