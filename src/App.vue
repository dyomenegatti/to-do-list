<template>
    <div id="app">
        <router-view/>
    </div>
</template>

<style>
@import '@/assets/styles/vars.css';

* {
    padding: 0;
    margin: 0;
    box-sizing: border-box;
    font-family: var(--font-poppins);
}

#app {
    font-family: var(--general-font);
    background: var(--background);
    color: var(--general-text);
    height: 100vh;
    width: 100vw;
}
</style>
