<template>
      <div class="news-contact-container">
        <div class="contacto">
          <p>Contacto</p>
          <form @submit.prevent="sendEmail">
            <div class="form-group">
              <label for="name">Nombre:</label>
              <input 
                type="text" 
                id="name" 
                v-model="formData.name"
                required
              />
            </div>
    
            <div class="form-group">
              <label for="email">Email:</label>
              <input 
                type="email" 
                id="email" 
                v-model="formData.email"
                required
              />
            </div>
    
            <div class="form-group">
              <label for="message">Mensaje:</label>
              <textarea 
                id="message" 
                v-model="formData.message"
                rows="5"
                required
              ></textarea>
            </div>
    
            <button type="submit">Enviar</button>
          </form>
        </div>
      </div>
    </template>
    
    <script>
    export default {
      data() {
        return {
          formData: {
            name: '',
            email: '',
            message: ''
          }
        };
      },
      methods: {
        sendEmail() {
          const mailtoLink = `mailto:gfreire96@gmail.com?subject=Mensaje de ${encodeURIComponent(this.formData.name)}&body=Nombre: ${encodeURIComponent(this.formData.name)}%0AEmail: ${encodeURIComponent(this.formData.email)}%0AMensaje: ${encodeURIComponent(this.formData.message)}`;
          window.location.href = mailtoLink;
        }
      }
    };
    </script>
    
    <style scoped>
    .contacto {
      width: 100%;
      max-width: 100%;
      margin-top: 1rem;
      padding: 15px;
      background-color: #fff;
      box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
      border-radius: 8px;
    }
    
    .form-group {
      margin-bottom: 1rem;
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
      transition: background-color 0.3s ease;
    }
    
    .contacto button:hover {
      background-color: #218838;
    }
    </style>
    