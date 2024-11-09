<script setup>
import icono1 from '/src/assets/mu.png';
import icono2 from '/src/assets/ecomerce.svg';
import icono3 from '/src/assets/configuracion.svg';
import icono4 from '/src/assets/uiux.svg';
import icono5 from '/src/assets/watch.svg';

import { ref } from 'vue';
const titulo = 'Consultoria freelance';
const fecha = '2020';
const experiencias = ref([
    { id: 1, src: icono1, parrafo: 'Colaboración freelance en el equipo de desarrollo de la Dirección Provincial de Ganadería del gobierno de la provincia de Mendoza para el desarrollo de sistemas de marcas y señales ganaderas, y sistema de emisión de guías de traslado de animales/autogestión.' },]);
</script>

<template>
    <h2>Experiencia</h2>
    <div class="card">
        <h3 class="titulo">{{ titulo.toLocaleUpperCase() }}</h3>
        <p class="fecha">{{ fecha }}</p>
        <ul class="listado">
            <li class="item" v-for="experencia in experiencias" :key="experencia.id">
                <img class="imagen-svg" :src="experencia.src" width="90rem" :alt="experencia.parrafo">
                <p>{{ experencia.parrafo }}</p>
            </li>

            <!-- <li class="item"><img class="imagen-svg" src="/src/assets/ventas.svg" width="45rem" alt="">
                <p>Lideré un equipo de 5 desarrolladores en la creación de una plataforma de comercio electrónico que incrementó las ventas en un 35% durante el primer año.</p>
            </li>
            <li class="item"><img class="imagen-svg" src="/src/assets/ecomerce.svg" width="45rem" alt="">
                <p>Diseñé y desarrollé aplicaciones web utilizando Node.js, React y MongoDB, logrando reducir el tiempo de carga de las páginas en un 50%.</p>
            </li>
            <li class="item"><img class="imagen-svg" src="/src/assets/configuracion.svg" width="45rem" alt="">
                <p>Implementé soluciones de autenticación y autorización, mejorando la seguridad del sitio web y reduciendo los intentos de acceso no autorizado en un 20%.</p>
            </li>
            <li class="item"><img class="imagen-svg" src="/src/assets/uiux.svg" width="45rem" alt="">
                <p>Colaboré con diseñadores de UX/UI para crear interfaces de usuario atractivas y fáciles de usar, aumentando la satisfacción del cliente en un 15%.</p>
            </li>
            <li class="item"><img class="imagen-svg" src="/src/assets/watch.svg" width="45rem" alt="">
                <p>Automaticé procesos de despliegue continuo utilizando Jenkins y Docker, reduciendo los tiempos de despliegue en un 40%.</p>
            </li> -->
        </ul>
    </div>
</template>

<style scoped>
h2 {
    color:#ff4500;
    text-align: left;
}

p{
    color: #F1EFF0;
    text-align: justify;
}
.card {
    display: flex;
    flex-direction: column;
    padding: 2rem;
    background-color: #d13801;
    border-radius: 15px;
}

.titulo {
    font-size: 1.5rem;
    color: rgb(255, 162, 129);
}

.fecha {
    font-size: 2.5rem;
    color: rgb(218, 194, 164);
    margin-bottom: 1rem;
}

.listado {
    display: flex;
    flex-direction: column;
}

.item {
    align-items: center;
    display: flex;
    padding: 1rem;
    gap: 1.5rem;
}
</style>