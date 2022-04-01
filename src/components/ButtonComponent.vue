<template>
    <div class="hello">
        <div class="btn-container">
            <button v-on:click="incrementCount">{{ counter }}</button>
            <h1>{{ count }}</h1>
            <button v-on:click="resetCount">{{ erase }}</button>
        </div>
    </div>
</template>

<script>
export default {
    name: "ButtonComponent",
    data() {
        return {
            counter: "Contar",
            count: 0,
            erase: "Borrar",
        };
    },
    methods: {
        incrementCount() {
            this.count++;
        },
        resetCount() {
            this.count = 0;
        },
    },
};
</script>

<style scoped>
.btn-container {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    text-align: center;
    font-family: var(--main-font);
}
</style>
