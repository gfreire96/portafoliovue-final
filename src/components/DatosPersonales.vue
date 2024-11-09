<script setup>
import FormularioContacto from './FormularioContacto.vue';

const presentacion = 'Soy Gabriel Freire Parola, programador y estudiante de física en UNSL y de programación en UTN San Rafael. Con un perfil generalista pero enfoque en backend, busco integrar conocimientos técnicos para desarrollar soluciones innovadoras';


/*<div class="news-contact-container">
    <div class="contacto">
        <p>Contacto</p>
        <form id="contactForm">
            <label for="name">Nombre:</label>
            <input type="text" id="name" name="name" required />
            <label for="email">Email:</label>
            <input type="email" id="email" name="email" required />
            <label for="message">Mensaje:</label>
            <textarea id="message" name="message" rows="5" required></textarea>
            <button type="submit">Enviar</button>
        </form>
    </div>
</div>*/
</script>

<template>
  <section class="datos-personales">
    <div class="about">
      <img class="img-perfil" src="/src/assets/perfil.jpg" alt="Foto de perfil" />
      <div class="card">
        <p>{{ presentacion }}</p>
      </div>
    </div>

   
   <FormularioContacto />



  </section>
</template>

<style scoped>
/* General Styles */
h1 {
  font-size: 2.5rem;
}

p {
  color: #F1EFF0;
  font-size: 1.5rem;
  font-weight: 400;
  margin-bottom: 1rem;
}

.card {
  background-color: rgb(19, 94, 184);
  border-radius: 15px;
  padding: 10px;
  text-align: justify;
}

.about {
  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: justify;
  line-height: 1.6;
}

.img-perfil {
  margin-bottom: 1rem;
  border-radius: 10%;
  max-width: 100%;
  height: auto;
  width: auto;
}

/* Contact Form */
/*.contacto {
  width: 100%;
  max-width: 100%;
  margin-top: 1rem;
  padding: 15px;
  background-color: #fff;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
  border-radius: 8px;
}

.contacto input,
.contacto textarea {
  width: 100%;
  padding: 10px;
  margin-top: 5px;
  border: 1px solid #ccc;
  border-radius: 5px;
  font-size: 1rem;
}

.contacto button {
  width: 100%;
  padding: 10px;
  margin-top: 20px;
  background-color: #0d0c0b;
  color: #fff;
  border: none;
  border-radius: 5px;
  cursor: pointer;
  font-size: 1rem;
  font-weight: bold;
}

.contacto button:hover {
  background-color: #218838;
}
*/

/* Responsive Adjustments */
@media (min-width: 768px) {
  .about {
    flex-direction: row;
    justify-content: space-between;
  }

  .img-perfil {
    margin-right: 2rem;
    margin-bottom: 0;
    height: auto;
    width: auto;
  }
}
</style>
