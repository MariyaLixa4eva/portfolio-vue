<template>
    <div class="error">
        <div class="container">
            <div class="error-text">
                <!-- <h2>{{ $t("error.title") }}</h2> -->
                <h2>404</h2>
            </div>
            <div class="error-info">
                <h3>{{ $t("error.text") }}</h3>
                <button><router-link to="/">{{ $t("error.btn") }}</router-link></button>
            </div>
        </div>
    </div>
</template>
<style scoped>
.error {
    width: 100%;
}
.container {
    margin: 0 auto;
    max-width: 1200px;
    padding: 20px;
}
.error-text {
    margin-top: 100px;
    text-align: center;
}
h2  {
    color: var(--bg);
    position: relative;
    margin-bottom: 50px;
    font-size: 10rem;
    -webkit-text-stroke: 0.1px var(--color);
    text-shadow: 1px 1px 6px var(--color);
}
h2::after  {
    content: '';
    position: absolute;
    width: 220px;
    height: 220px;
    background-color: rgb(25, 32, 57, 0.6);
    border-radius: 5px;
    left: 35%;
    transform: rotate(30deg);
    z-index: -1;
    border: 0.5px solid var(--color);
}
h2::before  {
    content: '';
    position: absolute;
    width: 200px;
    height: 200px;
    background-color: rgb(25, 32, 57, 0.6);
    border-radius: 5px;
    left: 40%;
    z-index: -1;
    transform: rotate(15deg);
    border: 0.5px solid var(--color);
}
.error-info {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 50px;
}
h3 {
    font-size: 2rem;
    color: white;
}
button {
    background-color: var(--bg);
    padding: 10px 30px;
    margin: 13px;
    color: #fff;
    border: none;
    border-radius: 5px;
    box-shadow: 0 0 5px var(--color), 0 0 20px var(--color);
    text-transform: uppercase;
}
@media all and (max-width: 600px) {
    h2  {
        font-size: 4rem;
    }
    h2::before {
        width: 90px;
        height: 90px;
    }
    h2::after {
        width: 80px;
        height: 80px;
    }
    h3 {
        font-size: 1rem;
    }
    h4 {
        font-size: 2rem;
    }
    .error-card svg {
        width: 40px;
        height: 40px;
    }
}
</style>