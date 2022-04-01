<template>
    <HeaderComponent />
    <ButtonComponent />
</template>

<script>
import ButtonComponent from "./components/ButtonComponent.vue";
import HeaderComponent from "./components/HeaderComponent.vue";

export default {
    name: "App",
    components: {
        ButtonComponent,
        HeaderComponent,
    },
};
</script>

<style>
@import url(./assets/css/variables.css);
#app {
    animation: all 0.3s ease;
    font-family: var(--main-font);
    background-color: var(--bg-color);
    font-weight: 500;
    -webkit-font-smoothing: antialiased;
}

body {
    margin: 0;
    background-color: var(--bg-color);
}
</style>
