<template>
    <div class="about">
        <div class="container">
            <div class="about-img">
                <img alt="logo" src="../assets/girl.png" />
            </div>
            <div class="about-text">
                <h2>{{ $t("about.title") }}</h2>
                <p>{{ $t("about.text-one") }}</p>
                <p>{{ $t("about.text-two") }}</p>
                <p>{{ $t("about.text-three") }}</p>
            </div>
        </div>
    </div>
</template>
<style scoped>
.about {
    width: 100%;
    position: relative;
    display: flex;
    align-items: center;
}
.container {
    margin: 0 auto;
    max-width: 1200px;
    padding: 20px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-top: 8%;
}
.about-img {
    border: 3px solid white;
    position: relative;
    width: 40%;
    padding: 20px;
    border-radius: 3px;
}
.about-img img {
    width: 100%;
}
.about-img::after {
    content: '';
    width: 100%;
    height: 100%;
    left: 40px;
    top: 40px;
    position: absolute;
    z-index: -1;
    border: 3px solid var(--color);
    border-radius: 3px;
}
.about-text {
    width: 40%;
}
h2  {
    color: var(--bg);
    position: relative;
    margin-bottom: 50px;
    font-size: 4rem;
    -webkit-text-stroke: 0.3px var(--color);
    text-shadow: 1px 1px 6px var(--color);
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
p {
    color: white;
    margin-bottom: 10px;
}
@media all and (max-width: 1050px) {
    .about-text {
        width: 50%;
    }
}
@media all and (max-width: 1000px) {
    .container {
    margin: 0 auto;
    max-width: 1200px;
    padding: 20px;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    margin-top: 70px;
    }
    .about-img {
        width: 70%;
    }
    .about-text {
        width: 100%;
        margin-top: 50px;
    }
}
@media all and (max-width: 600px) {
    h2  {
        font-size: 2.5rem;
    }
}
@media all and (max-width: 500px) {
    .about-img {
        width: 60%;
        padding: 5px;
    }
    .about-img::after {
        left: 20px;
        top: 20px;
    }
}
</style>