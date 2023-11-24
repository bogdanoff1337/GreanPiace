<template>
  <div v-if="showModal" class="modal">
    <div class="modal-content">
    
      <form @submit.prevent="sendEmail">
        <input class="contact__input" type="text" v-model="name" name="name" placeholder="Your Name" />
        <input class="contact__input" type="email" v-model="email" name="email" placeholder="Your Email" />
        <input class="contact__input" name="message" v-model="message" cols="30" rows="5" placeholder="Message" />
        <button class="help__button" style="margin-top: 14px;" type="submit" value="Send">Send</button>
      </form>
      <button class="close-button" @click="closeModal">&times;</button>
    </div>
  </div>
</template>
  
  <script>
 import emailjs from 'emailjs-com';
  
  export default {
    props: {
    showModal: Boolean,
  },
  
    data() {
      return {
        name: '',
        email: '',
        message: '',
      
       
      };
    },
    methods: {
      sendEmail(e) {
        try {
        emailjs.sendForm('service_e8qpbdi', 'template_t5f4zec', e.target, 'GWRq3Vp1yZyGVjiIV', {
          name: this.name,
          email: this.email,
          message: this.message
        })

      } catch (err) {
           if (err instanceof ReferenceError) {
            alert( "JSON Error: " + err.message );
           } else {
            throw err; // rethrow
           }
      }
      
      this.name = ''
      this.email = ''
      this.message = ''
        this.closeModal(); 
      },
      openModal() {
        this.isModalOpen = true; 
      },
      closeModal() {
      this.$emit('close');
    },
    }
  };
  </script>
  
  <style scoped>
  .close-button {
  position: absolute;
  top: 10px;
  right: 10px;
  font-size: 20px;
  cursor: pointer;
  background: none;
  border: none;
  padding: 0;
  outline: none;
}

.modal {
  display: flex;
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.5);
  justify-content: center;
  align-items: center;
}

.modal-content {
  background-color: white;
  padding: 20px;
  border-radius: 8px;
  width: 50%;
  transition: width 0.3s ease-in-out; /* Додайте плавний перехід */
}

@media (max-width: 991px) {
  .modal-content {
    width: 300px;
  }
}
  .contact__input {
    text-align: center;
    width: 100%; 
    box-sizing: border-box; 
    margin-bottom: 10px; 
}
@media (max-width: 991px) {
  .contact__input {
    margin-top: 40px;
  }
}
.contact__input {
  border-radius: 61px;
  background-color: #9fdea9;
  align-self: stretch;
  display: flex;
  height: 56px;
  flex-direction: column;
}
.contact__email {
  border-radius: 61px;
  background-color: #9fdea9;
  align-self: stretch;
  display: flex;
  margin-top: 14px;
  height: 56px;
  flex-direction: column;
}
.contact__phone {
  border-radius: 61px;
  background-color: #9fdea9;
  align-self: stretch;
  display: flex;
  margin-top: 14px;
  height: 56px;
  flex-direction: column;
}

.help__button {
  color: #48924f;
  text-align: center;
  white-space: nowrap;
  border-radius: 35px;
  background: radial-gradient(50% 50% at 50% 50%, #fff 0%, #f9f9f9 100%);
  box-shadow: 0px 10px 50px 0px rgba(16, 51, 30, 0.5);
  align-self: center;
  margin-top: 100px;
  width: 180px;
  max-width: 100%;
  align-items: center;
  padding: 26px 20px;
  font: 700 18px Poppins, sans-serif;
  cursor: pointer;
}
.help__button:hover {
  background: radial-gradient(50% 50% at 50% 50%, #48924f 0%, #48924f 100%);
  color: #fff;
  box-shadow: 0px 0px 30px 0px rgba(16, 51, 30, 0.7);
  
  transition: all 0.7s ease-in-out;
}

@media (max-width: 991px) {
  .help__button {
    white-space: initial;
    margin-top: 40px;
  }
}
  </style>
  