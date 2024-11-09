<script setup>
import NavBar from './components/NavBar.vue';
import DatosPersonales from './components/DatosPersonales.vue';
import Educacion from './components/EducacionComponente.vue';
import ExperienciaComponente from './components/ExperienciaComponente.vue';
import ProyectosComponente from './components/ProyectosComponente.vue';
import HabilidadesComponente from './components/HabilidadesComponente.vue';
import InteresesComponente from './components/InteresesComponente.vue';
</script>

<template>
    <header id="top">
        <!--Barra de Navegacion-->
        <NavBar />
        <!--Componente Datos Personales-->
        <DatosPersonales />
    </header>
    <main>
        <!--el estilo css de section se encuentra en base.css-->
        <section id="educacion">
            <!--Componente Educación-->
            <Educacion />
        </section>
        <section id="experiencia">
            <!--Componente Experiencia-->
            <ExperienciaComponente />
        </section>
        <section id="proyectos">
            
            <!--Componente Proyectos-->
            <ProyectosComponente />
        </section>
        <section id="habilidades">
            <!--Componente Habilidades-->
            
            <HabilidadesComponente />
        </section>
        <section id="intereses">
            <!--Componente Intereses-->
            
            <InteresesComponente />
        </section>
    </main>
    <footer>
        <div class = 'footer-container'>
            <div class="footer-info">
                <p>&copy; 2024 Gabriel Freire Parola.</p>
                <p>☎ Mi Teléfono personal: +54 2625-660775</p>
            </div>
            <div class="footer-social">
                <a href="https://www.x.com/" target="_blank" aria-label="X">
                    <!-- Icono SVG de X-->
                    <svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" fill="#000000" version="1.1" id="Layer_1" width="24px" height="24px" viewBox="0 0 24 24" style="enable-background:new 0 0 24 24;" xml:space="preserve"><path d="M14.095479,10.316482L22.286354,1h-1.940718l-7.115352,8.087682L7.551414,1H1l8.589488,12.231093L1,23h1.940717  l7.509372-8.542861L16.448587,23H23L14.095479,10.316482z M11.436522,13.338465l-0.871624-1.218704l-6.924311-9.68815h2.981339  l5.58978,7.82155l0.867949,1.218704l7.26506,10.166271h-2.981339L11.436522,13.338465z"/></svg>
                </a>
                <a href="https://github.com/gfreire96" target="_blank" aria-label="GitHub">
                    <!-- Icono SVG de GitHub -->
                    <img src="/src/assets/github_icon.svg" alt="Icono de GitHub" width="48" height="48">
                </a>
                <a href="https://www.linkedin.com/in/tuusuario" target="_blank" aria-label="LinkedIn">
                    <!-- Icono SVG de LinkedIn -->
                    <img src="/src/assets/linkedin_icon.svg" alt="Icono de Linkedin" width="48" height="48">
                </a>
            </div>

        </div>
    </footer>
</template>

<style scoped>
footer {
  background-color: #0d0c0b;
  color: #F1EFF0;
  height: 200px;
  width: 100%; /* Asegura que el footer ocupe el ancho completo de la ventana */
  display: flex;
  align-items: center;
  justify-content: center;
  margin-top: auto;
}


</style>
