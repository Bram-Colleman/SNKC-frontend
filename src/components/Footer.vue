<script setup>
const emit = defineEmits(["view"]);

function changeView(page) {
  emit("view", page);
}
</script>

<template>
    <div class="footer">

        <div class="row">
            <div class="logo__container" @click="changeView('home')">
                <img src="../assets/logo.png" alt="">
                <h3>Lid van de Vlaamse Karate Federatie</h3>
            </div>
            <div class="sponsors">
                <div class="sponsor sponsor__kine">
                    <a href="https://praktijk.fit" target="_blank">
                        <img src="../assets/praktijkfit.png" alt="" class="rounded logo__kine" >
                    </a>
                    <span>Osteopathie en sportkinisitherapie; dankzij onze combinatie van specialisaties bieden we jou een completere behandeling aan.</span>
                </div>
                <div class="sponsor sponsor__list">
                    <img src="../assets/Agri.png" alt="" class="rounded logo__agri filters" >
                    <img src="../assets/TTelektro.png" alt="" class="rounded logo__agri" >
                    <img src="../assets/Vaerewyck.png" alt="" class="rounded logo__agri" >
                </div>
            </div>
        </div>
        <div>
            <div class="tab__container">
                <p @click="changeView('actueel')">Actueel</p>
                <p @click="changeView('overons')">Onze club</p>
                <p @click="changeView('kata')">Kata</p>
                <p @click="changeView('kumite')">kumite</p>
                <p @click="changeView('contact')">Contact</p>
            </div>
        </div>

    </div>
</template>

<style scoped>
.footer {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    background-color: rgb(35, 35, 35);
    color: white;
    padding: 2rem 5rem;
    margin-top: 5rem;
}
.row {
    display: flex;
    flex-direction: row;
}
.rounded {
    border-radius: .5rem;
}
.logo__kine {
    height: 3rem;
    margin-right: 1rem;
}
.logo__agri {
    max-width: 25%;
    max-height: 15rem;
}
.filters {
    filter: invert(1);
}

.logo__container {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    text-align: center;
    width: 75%;
}

.logo__container h3 {
    font-weight: normal;
}

.tab__container p {
    padding: 1rem 1rem 0 1rem;
}

.tab__container p:hover {
    text-decoration: underline;
    cursor: pointer;
}
.tab__container {
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: space-evenly;
    margin: 0 10rem;
    /* border-top: 1px lightgray solid; */
}

.sponsor {
    display: flex;
    align-items: center;
    margin: 1rem 0;
}
.sponsor__list {
    justify-content: space-evenly;
}

.sponsor__kine {
    margin-bottom: 2rem;
}
</style>
