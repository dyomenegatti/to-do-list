<template>
    <div id="app">
        <div class="app_container">
            <router-view/>
        </div>
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

.app_container {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100%;
}
</style>
