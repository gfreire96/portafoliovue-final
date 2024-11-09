<script setup>
import { ref } from 'vue';
import FondoLava from './FondoLava.vue';

const intereses = ref([
    'Soy un perfil generalista en desarrollo: Mis intereses abarcan gran parte del espectro, que va desde los electrones hasta los bits.',
    'Estudio física y, a su vez, programación, lo que me lleva a explorar temas tanto científicos como tecnológicos.',
    'En un día me encuentro pensando desde la conservación de energía en sistemas hasta cómo implementar un `div` en HTML.',
    'La división ricardiana del trabajo me impulsa a iterar sobre aplicaciones focales dentro de este espectro.',
    'Tal vez en un futuro cercano, este enfoque se materialice en forma de un emprendimiento.'
]);

</script>

<template>
    <h2>Intereses</h2>
    <div class="intereses-contenedor">
        <img class="img-compu" src="/src/assets/compu.jpg" alt="Foto de perfil" />
        <FondoLava height="auto" width="100%">
            <div class="contenedor-lista">
                <ul>
                    <li class="item" v-for="interes in intereses" :key="interes">
                        {{ interes }}
                    </li>
                </ul>
            </div>
        </FondoLava>
    </div>
</template>

<style scoped>
.img-compu {
    max-width: 34%;
    max-height: 34%;
    border-radius: 15px;
    margin-right: 1rem;
}

.intereses-contenedor {
    display: flex;
    align-items: flex-start;
    margin: 0 auto;
    max-width: 85%;
    padding: 1rem;
}

.contenedor-lista {
    list-style-type: none;
    padding: 1rem;
    margin-bottom: .5rem;
    color: var(--vt-c-white-soft);
    font-size: 1.4rem;
    text-shadow: 3px 3px 6px rgba(0, 0, 0, 1);
}

.item {
    margin-bottom: 1rem;
}

h2 {
    color: #32a852;
    text-align: left;
}
</style>
