<template>
    <nav class="navbar">
      <div class="navbar-menu">
        <div class="navbar-brand">
          <a href="#" class="navbar-item">🫂</a>
        </div>
        <div class="navbar-nav" :class="{ 'open': isNavbarOpen }">
          <ul class="nav-list" v-if="!isMobile">
            <li class="nav-item" v-for="nav in navegacion" :key="nav.nombre">
              <a :href="nav.enlace" class="nav-link" :style="{ '--hover-color': nav.hoverColor }">{{ nav.nombre }}</a>
            </li>
          </ul>
          <select class="nav-select" v-if="isMobile" v-model="selectedNav" @change="navigateTo(selectedNav)">
            <option value="" disabled selected>Menú</option>
            <option v-for="nav in navegacion" :key="nav.id" :value="nav.enlace">
              {{ nav.nombre }}
            </option>
          </select>
        </div>
      </div>
    </nav>
  </template>
  
  <script setup>
  import { ref, computed } from 'vue';
  
  const navegacion = ref([
    { id: 1, nombre: 'Educación', enlace: '#educacion', hoverColor: '#8b0000' },  
    { id: 2, nombre: 'Experiencia', enlace: '#experiencia', hoverColor: '#ff4500' }, 
    { id: 3, nombre: 'Proyectos', enlace: '#proyectos', hoverColor: '#ffa500' }, 
    { id: 4, nombre: 'Habilidades', enlace: '#habilidades', hoverColor: '#5f9ea0' },  
    { id: 5, nombre: 'Intereses', enlace: '#intereses', hoverColor: '#32a852' }  
  ]);
  
  const isNavbarOpen = ref(false);
  const selectedNav = ref('');
  
  const navigateTo = (link) => {
    if (link) {
      window.location.href = link;
    }
  };
  
  const isMobile = computed(() => {
    return window.innerWidth <= 768;
  });
  </script>
  
  <style scoped>
  .navbar {
    color: #0d0c0b;
    padding: 1rem 1rem;
    align-items: center;
  }
  
  .navbar-menu {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  
  .navbar-brand {
    font-size: 1.5rem;
    font-weight: bold;
  }
  
  .nav-list {
    list-style: none;
    display: flex;
    padding: 0;
    margin: 0;
  }
  
  .nav-item {
    margin-right: 1rem;
  }
  
  .nav-link {
    border: 1px solid #0d0c0b;
    border-radius: 5px;
    text-decoration: none;
    transition: 0.7s;
    padding: 10px;
    color: #0d0c0b;
  }
  
  .nav-link:hover {
    background-color: var(--hover-color);
    border-color: var(--hover-color);  /* Cambia el color del borde */
    color: #F1EFF0;
  }
  
  .nav-select {
    border: 1px solid #0d0c0b;
    border-radius: 5px;
    background-color: #F1EFF0;
    color: #0d0c0b;
    padding: 0.5rem 1rem;
    font-size: 1rem;
    cursor: pointer;
    transition: 0.6s;
    display: block;
    width: 100%;
    margin-bottom: 1rem;
  }
  
  .nav-select:hover {
    background-color: #0d0c0b;
    color: #F1EFF0;
  }
  
  @media (max-width: 768px) {
    .nav-list {
      display: none;
    }
  }
  </style>
  