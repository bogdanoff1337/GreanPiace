
<template>
  <vue-bar>
  <div class="div">
    <!-- header -->
    <div class="hero">
          <img
            loading="lazy"
            src="./img/hero.jpg"
            class="hero__image"
          />
          <div class="hero__content">
            <div class="hero__block">
              <img
                loading="lazy"
                src="./img/lawncare.png"
                class="hero__image-2"
              />
              <div class="hero__text">Round Rock<br /><strong>Yard Maintenance</strong></div>
              
            </div>
              <div class="hero__description">Lorem Ipsum is simply dummy</div>
              <div class="hero__info">Lorem ipsum<br />Lorem</div>
              <div class="help__button"  @click="openModal">Help Me</div>
          </div>
    </div>
    <contact-modal :showModal="isContactModalOpen" @close="closeModal" />
<!-- Services -->
    <div class="services">Services</div>
    
  <div class="services__heading">
    <div class="services__content">
      <!-- Стрілки для перегляду назад та вперед -->
      <div class="slider__arrow slider__arrow--prev" @click="prevSlide">&lt;</div>

      <transition name="fade" mode="out-in">
        <div :key="cards[currentIndex].id" class="services__item">
      
        <div class="services__card">
          <img
            loading="lazy"
            :src="cards[currentIndex].srcSet"
            class="services__img"
            :alt="`Card ${cards[currentIndex].id}`"
          />
          <div class="services__description">
            <div class="services__title">{{ cards[currentIndex].title }}</div>
            <div class="services__text">{{ cards[currentIndex].text }}</div>
          </div>
      
        </div>
      </div>
    </transition>
      <!-- Стрілки для перегляду назад та вперед -->
      <div class="slider__arrow slider__arrow--next" @click="nextSlide">&gt;</div>
    </div>
  </div>
 <!-- About -->
          <div class="help__button" style="margin-top: 50px;" @click="openModal">Help Me</div>
          <div class="about__title">About Us</div>
    <div class="about__content">
      <img
        loading="lazy"
        src="./img/png.png"
        class="about__img"
      />
      <div class="about__columns">
          <div class="about__section">
            <div class="about__column">
              <div class="about__description">
                Lorem Ipsum is simply dummy text of the printing and typesetting
                industry. Lorem Ipsum has been the industry's standard dummy
                text ever since the 1500s, when an unknown printer took a galley
                of type and scrambled it to make a type specimen book. It has
                survived not only five centuries, but also the leap into
                electronic typesetting, remaining essentially unchanged. It was
                popularised in the 1960s with the release of Letraset sheets
                containing Lorem Ipsum passages, and more recently with desktop
                publishing software like Aldus PageMaker including versions of
                Lorem Ipsum.
              </div>
            </div>
            <div class="about__column">
              <div class="about__description">
                Lorem Ipsum is simply dummy text of the printing and typesetting
                industry. Lorem Ipsum has been the industry's standard dummy
                text ever since the 1500s, when an unknown printer took a galley
                of type and scrambled it to make a type specimen book. It has
                survived not only five centuries, but also the leap into
                electronic typesetting, remaining essentially unchanged. It was
                popularised in the 1960s with the release of Letraset sheets
                containing Lorem Ipsum passages, and more recently with desktop
                publishing software like Aldus PageMaker including versions of
                Lorem Ipsum.
              </div>
            </div>
            <div class="about__column">
              <div class="about__description">
                Lorem Ipsum is simply dummy text of the printing and typesetting
                industry. Lorem Ipsum has been the industry's standard dummy
                text ever since the 1500s, when an unknown printer took a galley
                of type and scrambled it to make a type specimen book. It has
                survived not only five centuries, but also the leap into
                electronic typesetting, remaining essentially unchanged. It was
                popularised in the 1960s with the release of Letraset sheets
                containing Lorem Ipsum passages, and more recently with desktop
                publishing software like Aldus PageMaker including versions of
                Lorem Ipsum.
              </div>
            </div>
          
        </div>
        <div class="help__button" style="margin-top: 50px;"  @click="openModal">Help Me</div>
      </div>
    </div>

     <!-- Testymonials -->
    <div class="testimonials">Testymonials</div>
    <div class="testimonials__container">
      <div class="testimonials__item">
        <div class="testimonials__content">
          <div class="testimonial-inner">
              <div class="testimonial-avatar">
                <div class="testimonials__avatar">
                  <img
                    loading="lazy"
                    src="./img/avatar.jpg"
                    class="testimonials__avatar-img"
                  />
                </div>
                <div class="testimonial-person">
                  <div class="testimonials__text">
                    <div class="testimonials__name">Courtney Henry</div>
                    <div class="testimonials__description">
                      Lorem Ipsum is simply dummy text of the printing and
                      typesetting industry. Lorem Ipsum has been the industry's
                      standard dummy text ever since the 1500s, when an unknown
                      printer took a galley of type and scrambled it to make a
                      type specimen book
                    </div>
                  </div>
                </div>
              </div>  
            <img
              loading="lazy"
              src="https://cdn.builder.io/api/v1/image/assets/TEMP/1212da89-faf3-4a55-9851-7a6d0c3036b2?"
              class="testimonials__image"
            />
          </div>
        </div>

        <div class="testimonials__content">
          <div class="testimonial-inner">
              <div class="testimonial-avatar">
                <div class="testimonials__avatar">
                  <img
                    loading="lazy"
                    src="./img/avatar.jpg"
                    class="testimonials__avatar-img"
                  />
                </div>
                <div class="testimonial-person">
                  <div class="testimonials__text">
                    <div class="testimonials__name">Courtney Henry</div>
                    <div class="testimonials__description">
                      Lorem Ipsum is simply dummy text of the printing and
                      typesetting industry. Lorem Ipsum has been the industry's
                      standard dummy text ever since the 1500s, when an unknown
                      printer took a galley of type and scrambled it to make a
                      type specimen book
                    </div>
                  </div>
                </div>
              </div>  
            <img
              loading="lazy"
              src="https://cdn.builder.io/api/v1/image/assets/TEMP/1212da89-faf3-4a55-9851-7a6d0c3036b2?"
              class="testimonials__image"
            />
          </div>
        </div>
      </div>
    
    
      <div class="testimonials__item">
        <div class="testimonials__content">
          <div class="testimonial-inner">
              <div class="testimonial-avatar">
                <div class="testimonials__avatar">
                  <img
                    loading="lazy"
                    src="./img/avatar.jpg"
                    class="testimonials__avatar-img"
                  />
                </div>
                <div class="testimonial-person">
                  <div class="testimonials__text">
                    <div class="testimonials__name">Courtney Henry</div>
                    <div class="testimonials__description">
                      Lorem Ipsum is simply dummy text of the printing and
                      typesetting industry. Lorem Ipsum has been the industry's
                      standard dummy text ever since the 1500s, when an unknown
                      printer took a galley of type and scrambled it to make a
                      type specimen book
                    </div>
                  </div>
                </div>
              </div>  
            <img
              loading="lazy"
              src="https://cdn.builder.io/api/v1/image/assets/TEMP/1212da89-faf3-4a55-9851-7a6d0c3036b2?"
              class="testimonials__image"
            />
          </div>
        </div>
        <div class="testimonials__content">
          <div class="testimonial-inner">
              <div class="testimonial-avatar">
                <div class="testimonials__avatar">
                  <img
                    loading="lazy"
                    src="./img/avatar.jpg"
                    class="testimonials__avatar-img"
                  />
                </div>
                <div class="testimonial-person">
                  <div class="testimonials__text">
                    <div class="testimonials__name">Courtney Henry</div>
                    <div class="testimonials__description">
                      Lorem Ipsum is simply dummy text of the printing and
                      typesetting industry. Lorem Ipsum has been the industry's
                      standard dummy text ever since the 1500s, when an unknown
                      printer took a galley of type and scrambled it to make a
                      type specimen book
                    </div>
                  </div>
                </div>
              </div>  
            <img
              loading="lazy"
              src="https://cdn.builder.io/api/v1/image/assets/TEMP/1212da89-faf3-4a55-9851-7a6d0c3036b2?"
              class="testimonials__image"
            />
          </div>
        </div>
      </div>
    </div>
    <div class="contact">
      <div class="contact__container">
        <div class="contact__item">Contact Us</div>
        <div class="contact__content">
          <div class="contact-header">
            <div class="contact-column">
              <div class="contact__form">
                <contact-form />
              </div>
            </div>
            <div class="contact__side__bar">
              <div class="contact-container">
                <div class="contact-info">
                  <img
                    loading="lazy"
                    src="https://cdn.builder.io/api/v1/image/assets/TEMP/6b3d88ec-a56d-4913-bb60-5113f533c60d?"
                    class="img-14"
                  />
                  <div class="contact-detail">test@gmail.com</div>
                </div>
                <div class="contact-info">
                  <img
                    loading="lazy"
                    src="https://cdn.builder.io/api/v1/image/assets/TEMP/aee4466b-d947-4f20-ada0-9eb0719f3ca9?"
                    class="img-15"
                  />
                  <div class="contact-detail">(XXX) XXX-XXXX</div>
                </div>
                <div class="contact-info">
                  <img
                    loading="lazy"
                    src="https://cdn.builder.io/api/v1/image/assets/TEMP/c6e270cf-4fd1-4917-b00b-e060fe8163f1?apiKey=0c3d759e78b14f51937ec6585e1afc46&"
                    class="img-16"
                  />
                  <div class="contact-detail">
                    6666 Ash Dr. San Potebnya, South Ukraine 616
                  </div>
                </div>
              </div>
            </div>
          
          </div>
        </div>
      </div>
    </div>
    <div class="footer"> Created by Bohdan Panasiuk </div>
  </div>
</vue-bar>
</template>

<script>

import Vuebar from 'vuebar';
import ContactForm from './componets/ContactForm.vue'
import ContactModal from './componets/ContactModal.vue';

export default {
 
  data() {
    
    return {
      isContactModalOpen: false,
      currentIndex: 0,
      cards: [
        {
          id: 1,
          srcSet: "https://lh3.googleusercontent.com/pw/ADCreHcP42N3rdeud-HKTSn7h3pUA3OVEuGEY9U66BsWlR7UJl_v5WxybJSqHAHNLNesbX2DRmKZ47Z3GGDuh2u8s2QVg-JgLPw1KqaB2ByJ3_h2d1zA8LWs0HUqS9BUPgsmv7S6hQAL2Dc9ypd9mkiNBpbcl53GPWKx9UcpkLjkkmggoYZkbWtZKvbc01QU11aIMEUV3WCce9BTuJ98I5XDU_nbKZv0V7MZw_j78faYzxUy0jIdwccHyK5a34A7SJQ73wcH2FdQH5zY__-TC8fdF0KnhMb82Q58IRb2q4yQRJZuzaHXN9y3pKxc2TQAEVOfByYIgaHwViPgNyzSxKFgB6asjSolEtvm32_x7lJ83ecNwRGBLYZZCuG1WyYoh3tAm17wI-THCbNtyRhaxPLZIVHiFk1_clUQz4oJ2uKVgB0Ql2VspqSQeAcQwrCQc6O-fY7UUDsrZ7r75J6kOsuqheurwdCzMXQWsQiVxBxEpEmH4fsOSyI-RUoAfi-VS-vyFGAqzUgwyjRKlnMHGXo_FpeKxqkc6U0pUgsKDg4QPhKVZKlBkgAF0bIjIPqne65-1q1RMtluYzzl_TXa7p3GzonRh7mF9krIZ9qHrbWagR5DE0uotKcn2-KktSBkMlfy_Ve2bh9EhYiBBoucauc--gOK3tso4PZNAXmA-5WkpM2rGPmInItk-VfxXTDTXDFiCMDj7M4Xb-9knv4rZO6zmhuYoPutySzfnSEl21kMhL6id0SGLbu14T0iOWisTJ7w0qyG9t2KRJB1C24bIatZskmLWx-hzUimS3s0RCecNV4kE1mqDTsYu-X9d2rnUzeE8q9ZBAxN7K9XlOtZFj290NrsYCOZLRF2TpiXVt5QUyKiU85yuTa2Q0O6idi2lG0geeR_4nBvuJA_-2-gjCFF-PpSzFNSjJZFDk7vCq62-gY=w385-h290-s-no-gm?authuser=0",
          title: "Lorem Ipsum 1",
          text: "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled",
        },
        {
          id: 2,
          srcSet: "https://lh3.googleusercontent.com/pw/ADCreHfP71PJa3Vgs64RaOXdDPADo9YiEs1gs4hNAYHaXw2vQ2DyxnzGfIxLMSm0cw9975qzFgF-osG6dgI3PWODRmcISuAP8YQZwIVx8EzltRRpP1kU-DNN-RnZfeSgqLky54cEjcdt9Tzhnnij-JJfriZeM9x3v8bePynlKDfvYvj1SbuesMoFnjXj3SLeKeUmaTdGJHoL9Luzh7JvvOc7QbGka6mYlLDJCrmlhXCJiTI54cp0uxQF1L1s5cWxboCjkZM2RW9XJbsFASBhDOF5HsRbWY9J9I8dh8SwV4jakS-rnzSdcXhg_nZ2AmNyJpUjlVPXlSB8whTnVnOfftgRCFueHA6bRcv_0EvPlMuBYlLlBZrbRSuazYhIA_rCVnIMG9dlgnTI4bb7f6zxdgvhLIj0Lzxd68mMOk5xLfIfx9hTIQr1dEHuJ4MYeGckt0x-qT45s3URLeW894Odxirc-pZry0WfGKyo3beF2p5tjKfCYoQoDbWACy6VnhxLJ8ZgSYETTcM_nuR2iPe7HzDQbv8QvvQAWuFFIINJCNDhcJpXMsTAxxKVzFW7iu9VTW9dwgh2lYHOQhhS3s63RRb6bN1X7eu0rXA9XxO3UvYT7kLWDmuILkJ7RSdPy7acgZ6TDfvAWll62BQiZZwgexKLjzaYcLiY4sukR01BoKVs3bGo69Q8uF7yypzpG39gaSaPZv5bnuq-mhlQ5850e7sfKZa1jbW0aXzlp71WjdRzJ0KjdAGfKyPGyQXJgSn4t2xzwZ5OQ8DqbkbOZD-zhEnXKs_KqEcxk9c1wDcbsARN98Gs7kQNR21blSKrHFpH8DRlQ2xOT0qK7mxgOgf3QRFG2uIDo39BIJDOT3CGHIDpNJywsw710FJfWu8TiYn-zqtQ6Q5cB7YtcK9_8w-QzKSb2CROeMPjXyVNLI2X_3-ikwQ=w385-h290-s-no-gm?authuser=0",

          title: "Lorem Ipsum 2",
          text: "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled",
        },
         {
          id: 3,
          srcSet: "https://lh3.googleusercontent.com/pw/ADCreHfFqklW1UHU4JaH7MbQnHcaM14ImF2JLdGh3luI0ll_z7ssvrr3zDymkoSrr490e3RclCljGQ-WzyKLq1NQBtd0Tw0s9_WCxiesvc2Z2PCl1B9VjwIccgyj2IQXLYMuq5KIlWPxIClCcZtsbVfnAajU81N1CgFrQnQAnu2qAxOqwa9q-KySeJDyFS2tEIRCwM1EKpXGP8hduV4CZZ4h024TzTz_GklD2NQE-s_Ga0zZBJdVGawnoVOEQKry-SjDNdoE9K0WA6X_6cqa8qc2zhbSSdnFGrHLdQ0GE4zhLxpesTd6keS2PGyOGX9HuXCcyHWjwci_OVmppnjApIIbd56AkPjCMbvIWkFoqWd3SHwkHeUa1xTKCJehKflwbMzXtsKvCBJrIbDs1ZdI4gdICTFtVWxEOrC9mC_sjqbQObbrFdxST0vypgJhq9FRUaerNSqaJ5rMjfQxKAIJujfAOUly20nOFQoe-K7ypdUo_4XAWTAgAu6AiuALvx6NMJRlHRnmgVL2ZQV4F_d9zfuGjt5hjnJqfSkQ2kFaUKrJ84Q7z9w-K1lrt_vtMUYy4uXvUSNNbf9WfUi8KHKyaCNPyxccdRbLFuNTZ0SIfbwxAdmVJNRBtImtOhRfOD6ZE9DcaGbebiKOOJat1I58F2xkRSg7G51CxtfOXKP42cRPjSJ53DKmg4rnmCFl0CKqwse0nZO1e7WdxTytYdR5AfkH2zp6e9_uYBqfvkc3nf55OEUKSbEzF2pA7GzMdHIXwPo8nNHARWQZmeBTAuazW_7Vnq2eORmLIOvre_uudFhoYCu8-JtY2O0p6tvV56NwmqqqXFSoXVZRA43-QX2VmXWgiow2GYYTqnI5J6kon6-eHY6u872YCBKNsKCpZ651pId_eKOVaOb-j6BvH0L7OlyW9Y-k5JZOzA1pq_nLcxMJoeijr8ataZPK-W8MEtc6HVM=w385-h290-s-no-gm?authuser=0",
          title: "Lorem Ipsum 3",
          text: "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled",
        },
      ],
    };
  },

  methods: {
    prevSlide() {
      this.currentIndex = (this.currentIndex - 1 + this.cards.length) % this.cards.length;
    },

    nextSlide() {
      this.currentIndex = (this.currentIndex + 1) % this.cards.length;
    },
    openModal() {
      this.isContactModalOpen = true;
    },
    closeModal() {
      this.isContactModalOpen = false;
    }
  },


     
     
      components: {
       Vuebar,
       ContactForm,
       ContactModal,
    },
};

</script>



<style scoped>
.fade-enter-active, .fade-leave-active {
  transition: opacity 0.5s;
}
.fade-enter, .fade-leave-to {
  opacity: 0;
}
.services__heading {
  position: relative;
}

.slider__arrow {
  position: absolute;
  top: 50%;
  transform: translateY(-50%);
  font-size: 24px;
  cursor: pointer;
  color: #000; /* Колір стрілок */
}

.slider__arrow--prev {
  left: 10px;
}

.slider__arrow--next {
  right: 10px;
}

.div {
  background-color: #fff;
  display: flex;
  flex-direction: column;
}
.hero {
  display: flex;
  flex-direction: column;
  overflow: hidden;
  align-self: stretch;
  position: relative;
  display: flex;
  min-height: 840px;
  width: 100%;
  align-items: center;
 
}

@media (max-width: 991px) {
  .hero {
    max-width: 100%;
    padding-bottom: 100px;
  }
}

.hero__image {
  position: absolute;
  height: 100%;
  width: 100%;
  object-fit: cover;
  object-position: center;
}

.hero__content {
  position: relative;
  display: flex;
  margin-bottom: -23px;
  width: 983px;
  max-width: 100%;
  flex-direction: column;
  
}

@media (max-width: 991px) {
  .hero__content {
    margin-bottom: 10px;
  }
}

.hero__block {
  align-self: center;
  display: flex;
  width: 363px;
  max-width: 100%;
  
  gap: 20px;
  margin-top: 58px;
  
  
}

@media (max-width: 991px) {
  .hero__block {
    flex-wrap: wrap;
  }
}

.hero__image-2 {
  aspect-ratio: 0.93;
  object-fit: contain;
  object-position: center;
  width: 78px;
  
  overflow: hidden;
  max-width: 100%;
}

.hero__text {
  color: #fff;
  letter-spacing: 7.02px;
  align-self: start;
  flex-grow: 1;
  flex-basis: auto;
  font: 800 27px/118.5% Poppins, sans-serif;
  padding: 58px auto;
}

.hero__description {
  color: #fff;
  text-align: center;
  white-space: nowrap;
  border-radius: 59px;
  background-color: rgba(0, 0, 0, 0.5);
  align-self: center;
  margin-top: 50px;
  width: 374px;
  max-width: 100%;
  align-items: center;
  padding: 23px 20px;
  font: 500 18px Poppins, sans-serif;
}

@media (max-width: 991px) {
  .hero__description {
    white-space: initial;
    margin-top: 40px;
  }
}

.hero__info {
  color: #FFF;
  text-align: center;
  text-shadow: 0px 0px 40px rgba(0, 0, 0, 0.50);
  font-family: Poppins;
  font-size: 144px;
  font-style: normal;
  font-weight: 900;
  line-height: 134.5px; /* 93.403% */
  margin-top: 17px;
}

@media (max-width: 991px) {
  .hero__info {
    max-width: 100%;
    font-size: 40px;
  }
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

.services {
  color: var(--Gray-3, #828282);
  text-align: center;
  align-self: center;
  margin-top: 70px;
  white-space: nowrap;
  font: 800 64px Poppins, sans-serif;
}
@media (max-width: 991px) {
  .services {
    font-size: 40px;
    margin-top: 40px;
    white-space: initial;
  }
}
.services__heading {
  display: flex;
  justify-content: center;
  align-self: center;
  margin-top: 76px;
  width: 1199px;
  max-width: 100%;
  padding: 0 20px;
}
@media (max-width: 991px) {
  .services__heading {
    margin-top: 40px;
  }
}
.services__content {
  gap: 20px;
    width: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
}
@media (max-width: 991px) {
  .services__content {
    flex-direction: column;
    align-items: stretch;
    gap: 0px;
  }
} 
.services__item {
  display: flex;
  flex-direction: column;
  line-height: normal;
  width: 33%;
  margin-left: 0px;
}
@media (max-width: 991px) {
  .services__item {
    width: 100%;
  }
}
.services__card {
  border-radius: 30px;
  box-shadow: 0px 10px 30px 0px rgba(16, 51, 30, 0.1);
  background-color: #fff;
  display: flex;
  flex-grow: 1;
  padding-bottom: 35px;
  flex-direction: column;
  width: 100%;
  margin: 0 auto;
}
@media (max-width: 991px) {
  .services__card {
    margin-top: 22px;
  }
}
.services__img {
  aspect-ratio: 1.33;
  object-fit: contain;
  object-position: center;
  width: 100%;
  overflow: hidden;
}
.services__description {
  display: flex;
  margin-top: 37px;
  flex-direction: column;
  padding: 0 62px 0 30px;
}
@media (max-width: 991px) {
  .services__description {
    padding: 0 20px;
  }
}
.services__title {
  color: #0d4d14;
  font: 900 16px/150% Poppins, sans-serif;
}
.services__text {
  color: #0d4d14;
  margin-top: 10px;
  font: 400 14px/143% Poppins, sans-serif;
}

.about__img{
 
  position: absolute;
  height: 100%;
  width: 100%;
  object-fit: cover;
  object-position: center;

}

.about__title {
  color: var(--Gray-3, #828282);
  text-align: center;
  align-self: center;
  margin-top: 70px;
  white-space: nowrap;
  font: 800 64px Poppins, sans-serif;
}
@media (max-width: 991px) {
  .about__title {
    font-size: 40px;
    margin-top: 40px;
    white-space: initial;
  }
}
.about__content {
  display: flex;
  flex-direction: column;
  box-shadow: 0px 4px 50px 0px rgba(0, 0, 0, 0.25) inset;
  overflow: hidden;
  align-self: stretch;
  position: relative;
  display: flex;
  min-height: 732px;
  margin-top: 76px;
  width: 100%;
  align-items: center;
  
}
@media (max-width: 991px) {
  .about__content {
    max-width: 100%;
   
    margin-top: 40px;
  }
}
.about__columns {
  position: relative;
  display: flex;
  width: 1195px;
  max-width: 100%;
  flex-direction: column;
  padding: 158px 20px 50px;
}

.about__section {
  gap: 20px;
  display: flex;
}
@media (max-width: 991px) {
  .about__section {
    flex-direction: column;
    align-items: stretch;
    gap: 0px;
  }
}
.about__description {
  color: #fff;
  text-align: center;
  font: 600 18px/133% Poppins, sans-serif;
}
@media (max-width: 991px) {
  .about__description {
    margin-top: 40px;
  }
}
.about__column {
  display: flex;
  flex-direction: column;
  line-height: normal;
  width: 33%;
  margin-left: 0px;
}

@media (max-width: 991px) {
  .about__column {
    width: 100%;
  }
}




.testimonials {
  color: var(--Gray-3, #828282);
  text-align: center;
  align-self: center;
  margin-top: 70px;
  white-space: nowrap;
  font: 800 64px Poppins, sans-serif;
}
@media (max-width: 991px) {
  .testimonials {
    max-width: 100%;
    font-size: 40px;
    margin-top: 40px;
    white-space: initial;
  }
}
.testimonials__container {
  align-self: center;
  margin-top: 79px;
  width: 1199px;
  max-width: 100%;
}
@media (max-width: 991px) {
  .testimonials__container {
    margin-top: 40px;
  }
}
.testimonials__item {
  gap: 20px;
  display: flex;
}
@media (max-width: 991px) {
  .testimonials__item {
    flex-direction: column;
    align-items: stretch;
    gap: 0px;
  }
}
.testimonials__content {
  display: flex;
  flex-direction: column;
  line-height: normal;
  width: 50%;
  margin-left: 20px;
}
@media (max-width: 991px) {
  .testimonials__content {
    width: 100%;
    margin-left: 0;
  }
}
.testimonial-inner {
  border-radius: 40px;
  border: 1px solid #6cb981;
  background-color: #fff;
  display: flex;
  flex-grow: 1;
  flex-direction: column;
  width: 100%;
  margin: 0 auto 45px;
  
  padding: 30px;
}
@media (max-width: 991px) {
  .testimonial-inner {
    max-width: 90%;
    margin-top: 40px;
    padding: 0 20px;
   
  }
}

.testimonial-avatar {
  gap: 20px;
  display: flex;
}
@media (max-width: 991px) {
  .testimonial-avatar {
    flex-direction: column;
    align-items: stretch;
    gap: 0px;
  }
}
.testimonials__avatar {
  display: flex;
  flex-direction: column;
  line-height: normal;
  width: 16%;
  margin-left: 0px;
}
@media (max-width: 991px) {
  .testimonials__avatar {
    width: 100%;
  }
}
.testimonials__avatar-img {
  aspect-ratio: 1;
  object-fit: contain;
  object-position: center;
  width: 80px;
  overflow: hidden;
  border-radius: 50%;
  max-width: 100%;
}
@media (max-width: 991px) {
  .testimonials__avatar-img {
    margin-top: 14px;
  }
}
.testimonial-person {
  display: flex;
  flex-direction: column;
  line-height: normal;
  width: 84%;
  margin-left: 20px;
}
@media (max-width: 991px) {
  .testimonial-person {
    width: 100%;
  }
}
.testimonials__text {
  display: flex;
  margin-top: 4px;
  flex-grow: 1;
  flex-direction: column;
}
@media (max-width: 991px) {
  .testimonials__text {
    max-width: 100%;
    margin-top: 18px;
  }
}
.testimonials__name {
  color: #6cb981;
  white-space: nowrap;
  font: 700 18px/122% Poppins, sans-serif;
}
@media (max-width: 991px) {
  .testimonials__name {
    max-width: 100%;
    white-space: initial;
  }
}
.testimonials__description {
  color: #0d4c14;
  margin-top: 10px;
  font: 400 14px/157% Poppins, sans-serif;
}
@media (max-width: 991px) {
  .testimonials__description {
    max-width: 100%;
  }
}
.testimonials__image {
  aspect-ratio: 6.33;
  object-fit: contain;
  object-position: center;
  width: 114px;
  overflow: hidden;
  align-self: start;
  max-width: 100%;
  margin: 12px 0 0 94px;
}
@media (max-width: 991px) {
  .testimonials__image {
    margin-left: 10px;
    
  }
}

.contact {
  background-color: #fcfcfc;
  align-items: center;
  display: flex;
  margin-top: 50px;
  width: 100%;
  
  flex-direction: column;
  align-items: center;
  padding: 74px 20px 50px;
}
@media (max-width: 991px) {
  .contact {
    max-width: 100%;
    margin-top: 40px;
  }
}
.contact__container {
  display: flex;
  width: 786px;
  max-width: 100%;
  flex-direction: column;
  align-items: center;
}
.contact__item {
  color: var(--Gray-3, #828282);
  text-align: center;
  white-space: nowrap;
  font: 800 64px Poppins, sans-serif;
}
@media (max-width: 991px) {
  .contact__item {
    font-size: 40px;
    white-space: initial;
  }
}
.contact__content {
  align-self: stretch;
  margin-top: 96px;
}
@media (max-width: 991px) {
  .contact__content {
    max-width: 100%;
    margin-top: 40px;
  }
}
.contact-header {
  gap: 20px;
  display: flex;
}
@media (max-width: 991px) {
  .contact-header {
    flex-direction: column;
    align-items: stretch;
    gap: 0px;
  }
}
.contact-column {
  display: flex;
  flex-direction: column;
  line-height: normal;
  width: 55%;
  margin-left: 0px;
}
@media (max-width: 991px) {
  .contact-column {
    width: 100%;
  }
}
.contact__form {
  display: flex;
  flex-grow: 1;
  flex-direction: column;
  text-align: center;
}


.contact__form input {
    text-align: center;
    width: 100%; 
    box-sizing: border-box; 
    margin-bottom: 10px; 
}
@media (max-width: 991px) {
  .contact__form {
    margin-top: 40px;
  }
}
.contact__name {
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

.contact__side__bar {
  display: flex;
  flex-direction: column;
  line-height: normal;
  width: 45%;
  margin-left: 20px;
}
@media (max-width: 991px) {
  .contact__side__bar {
    width: 100%;
  }
}
.contact-container {
  display: flex;
  flex-direction: column;
    justify-content: space-between;
    max-width: 600px;
    margin: 0 auto;
}
@media (max-width: 991px) {
  .contact-container {
    margin-top: 40px;
  }
}
.contact-info {
  align-self: end;
  display: flex;
  margin-top: 30px;
  gap: 20px;
  text-align: center;
}
.img-14 {
  aspect-ratio: 1;
  object-fit: contain;
  object-position: center;
  width: 24px;
  overflow: hidden;
  max-width: 100%;
}
.contact-detail {
  color: var(--Gray-1, #333);
  align-self: center;
  white-space: nowrap;
  margin-top: 10px;
  font: 500 14px TT Hoves, sans-serif;
}
@media (max-width: 991px) {
  .contact-detail {
    white-space: initial;
  }
}

.img-15 {
  aspect-ratio: 1;
  object-fit: contain;
  object-position: center;
  width: 24px;
  overflow: hidden;
  max-width: 100%;
}


.img-16 {
  aspect-ratio: 1;
  object-fit: contain;
  object-position: center;
  width: 24px;
  overflow: hidden;
  max-width: 100%;
}

.footer {
  background-color: #324b29;
  align-self: stretch;
  display: flex;
  min-height: 145px;
  width: 100%;
  flex-direction: column;
  text-align: center;
  padding: 50px;
}
@media (max-width: 991px) {
  .footer {
    max-width: 100%;
  }
}
</style>