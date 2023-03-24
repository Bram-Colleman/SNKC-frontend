<script setup>
const emit = defineEmits(["view"]);

function changeView(page) {
  emit("view", page);
}
</script>

<template>
    <div class="nav-bar">
        <div class="logo__container" @click="changeView('home')">
            <img src="../assets/logo.png" alt="">
            <h2>Sint-Niklase Karateclub</h2>
        </div>
        <div class="tab__container">
            <p @click="changeView('actueel')">Actueel</p>
            <p @click="changeView('overons')">Onze club</p>
            <p @click="changeView('kata')">Kata</p>
            <p @click="changeView('kumite')">Kumite</p>
            <p @click="changeView('contact')">Contact</p>
        </div>
    </div>
</template>

<style scoped>
.nav-bar {
    display: flex;
    padding: 1rem 2rem;
    margin-bottom: 5rem;
    justify-content: space-between;
    background-color: #f1f1f1;
}

.logo__container, .tab__container {
    display: flex;
    flex-direction: row;
    align-items: center;
}
.logo__container img {
    height: 3rem;
    margin-right: 1rem;
}

.logo__container h2 {
    font-weight: normal;
}

.tab__container p {
    padding: 1rem 1rem;
    cursor: pointer;
}
.tab__container p:hover {
    opacity: 0.5;
    transition: 250ms;
}

.logo__container {
    cursor: pointer;
}
</style>
