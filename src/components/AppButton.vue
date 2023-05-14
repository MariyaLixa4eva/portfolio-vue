<template>
    <button
    >
        <slot />
    </button>
</template>

<style scoped>
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
</style>