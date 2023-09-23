<template>
  <div class="contact__main__wrapper">
    <div class="contact__main__wrapper__bg__blur">
      <div class="contact__main container">
        <div class="contact__info">
          <div class="contact__info__get-in-touch">Get in touch</div>
          <div class="contact__info__section">
            Contact <br />
            Information
          </div>
          <div class="contact__info__section">
            27,Alara Street <br />
            Yaba 100012 <br />
            Lagos State
          </div>
          <div class="contact__info__section">Call Us : 07067981819</div>
          <div class="contact__info__section">
            we are open from Monday-Friday <br />
            08:00am - 05:00pm
          </div>
          <div class="contact__info__section__share-on-wrapper">
            <div class="contact__info__section__share-on__text">Share on</div>
            <div class="contact__info__section__share-on__social-media__icons">
              <img src="@/assets/images/instagram.svg" alt="" />
              <img src="@/assets/images/X.svg" alt="" />
              <img src="@/assets/images/facebook.svg" alt="" />
              <img src="@/assets/images/linkedin.svg" alt="" />
            </div>
          </div>
        </div>
        <form class="contact__form" @submit.prevent="submit()">
          <h3 class="contact__form__heading">
            Questions or need assistance? <br />Let us know about it!
          </h3>
          <div class="contact__form__title">
            Email us below to any question related to our event
          </div>
          <div class="contact__form__input__group">
            <div class="contact__form__input__wrapper">
              <input
                name="First Name"
                type="text"
                placeholder="First Name"
                v-model="formData.first_name"
              />
            </div>
            <div class="contact__form__input__wrapper">
              <input
                name="E-Mail"
                type="email"
                placeholder="Mail"
                v-model="formData.email"
              />
            </div>
            <div class="contact__form__input__wrapper">
              <textarea
                name="Your Message"
                type="text"
                placeholder="Message"
                v-model="formData.message"
              ></textarea>
            </div>
          </div>
          <div v-if="showSuccess" class="contact__form__success-message">
            <div class="contact__form__success-message__title">Success</div>
            <div class="contact__form__success-message__text">
              Your form have been submit we will get back to you shortly
            </div>
          </div>
          <button
            :disabled="loading || !formIsValid"
            class="contact__form__submit-button"
          >
            <div class="spinner" v-if="loading"></div>
            <span v-else>Submit</span>
          </button>
          <div
            class="contact__info__section__share-on-wrapper contact__info__section__share-on-wrapper--pos-bottom"
          >
            <div class="contact__info__section__share-on__text">Share on</div>
            <div class="contact__info__section__share-on__social-media__icons">
              <img src="@/assets/images/instagram.svg" alt="" />
              <img src="@/assets/images/X.svg" alt="" />
              <img src="@/assets/images/facebook.svg" alt="" />
              <img src="@/assets/images/linkedin.svg" alt="" />
            </div>
          </div>
        </form>
      </div>
    </div>
  </div>
</template>

<script>
import RegistrationSuccessfulModal from "@/components/RegistrationSuccessfulModal.vue";
export default {
  components: { RegistrationSuccessfulModal },
  data() {
    return {
      baseUrl: "https://backend.getlinked.ai",
      categoriesList: [],
      formData: {
        email: "",
        phone_number: "",
        first_name: "",
        message: "",
      },
      loading: false,
      showSuccess: false,
    };
  },
  computed: {
    formIsValid() {
      let k = this.formData;
      return (
        k.email !== "" &&
        k.phone_number !== "" &&
        k.first_name !== "" &&
        k.message !== ""
      );
    },
  },
  methods: {
    async submit() {
      try {
        this.loading = true;
        let res = await fetch(`${this.baseUrl}/hackathon/contact-form`, {
          method: "POST",
          headers: {
            "Content-Type": "application/json",
          },
          body: JSON.stringify(this.formData),
        });
        let response = await res.json();
        if (!res.ok) {
          throw new Error("Network response was not ok");
        }
        this.showSuccess = true;
      } catch (error) {
        console.error(error);
        alert("Opps There was an error");
      } finally {
        this.loading = false;
      }
    },
  },
};
</script>

<style scoped>
.contact__main__wrapper {
  background: #150e28;
  background-position: 0% 100px, 100% 100%;
  background-image: url(@/assets/images/Purple-Lens-Flare-PNG.png),
    url(@/assets/images/Purple-Lens-Flare-PNG.svg);
  background-blend-mode: hard-light;
  background-repeat: no-repeat;
  background-size: 760px 560px;
}
.contact__main__wrapper__bg__blur {
  backdrop-filter: blur(80px);
  padding-top: 185px;
}
.contact__main {
  display: flex;
  flex-wrap: wrap;
  min-height: calc(100vh - 185px);
  align-items: center;
  justify-content: center;
  gap: 225px;
  max-width: 1350px;

  background-position: 7% 10%, 87% 0%, 45.1% 76%, 0% 33%, 36% 37%;
  background-image: url(@/assets/images/register-form-gradient-star.svg),
    url(@/assets/images/register-form-star-lightgrey.svg),
    url(@/assets/images/register-form-purple-star.svg),
    url(@/assets/images/register-form-outline-star.svg),
    url(@/assets/images/register-form-outline-star.svg);
  background-blend-mode: hard-light;
  background-repeat: no-repeat;
}
.contact__info {
  width: 272px;
  height: fit-content;
  display: flex;
  flex-direction: column;
  gap: 17px;
}
.contact__info__get-in-touch {
  color: #d434fe;
  font-family: Clash Display;
  font-size: 32px;
  font-style: normal;
  font-weight: 600;
  line-height: normal;
}
.contact__info__section {
  color: #fff;
  font-family: Montserrat;
  font-size: 16px;
  font-style: normal;
  font-weight: 400;
  line-height: normal;
}
.contact__info__section__share-on-wrapper {
  margin-top: 35px;
}
.contact__info__section__share-on__text {
  color: #d434fe;
  font-family: Montserrat;
  font-size: 16px;
  font-style: normal;
  font-weight: 400;
  line-height: normal;
}
.contact__info__section__share-on-wrapper--pos-bottom {
  display: flex;
  flex-direction: column;
  align-items: center;
  margin-top: 41px;
  display: none;
}
.contact__info__section__share-on__social-media__icons {
  margin-top: 14px;
  display: flex;
  align-items: center;
  gap: 16.5px;
}
.contact__form {
  max-width: 617px;
  flex: 1;
  padding: 65px 91px;
  border-radius: 12px;
  background: rgba(255, 255, 255, 0.03);
  box-shadow: 0px 4px 4px 0px rgba(0, 0, 0, 0.25);
}
.contact__form__heading {
  color: #d434fe;
  font-family: "Clash Display";
  font-size: 20px;
  font-weight: 600;
  line-height: normal;
  margin-bottom: 46px;
}
.contact__form__title {
  color: #fff;
  font-family: Montserrat;
  font-size: 12px;
  font-style: normal;
  font-weight: 400;
  line-height: normal;
  margin-top: 24px;
  margin-bottom: 30px;
  display: none;
}
.contact__form__input__wrapper {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}
.contact__form__input__wrapper input,
.contact__form__input__wrapper textarea {
  color: #fff;
  font-family: Montserrat;
  font-size: 16px;
  font-style: normal;
  font-weight: 400;
  line-height: normal;
  height: 47px;
  border-radius: 4px;
  border: 1px solid #fff;
  background: rgba(255, 255, 255, 0.03);
  box-shadow: 0px 4px 4px 0px rgba(0, 0, 0, 0.25);
  padding: 13px 29px;
  outline: none;
  margin-bottom: 42px;
}
.contact__form__input__wrapper textarea {
  height: 119px;
  margin-bottom: 31px;
}
.contact__form__input__wrapper select {
  appearance: none;
  background-repeat: no-repeat;
  background-position: right 13.5px center;
  background-image: url("@/assets/images/select-arrow-down.svg");
}
.contact__form__input__wrapper input::placeholder,
.contact__form__input__wrapper textarea::placeholder {
  color: #fff;
}
.contact__form__success-message {
  width: 100%;
  padding: 16px;
  background-color: rgba(15, 126, 15, 0.359);
  border-radius: 4px;
  border: 2px solid green;
  color: green;
  margin-bottom: 31px;
}
.contact__form__success-message__title {
  font-weight: 600;
  margin-bottom: 8px;
}
.contact__form__success-message__text {
}
.contact__form__submit-button {
  color: #fff;
  font-family: Montserrat;
  font-size: 16px;
  font-weight: 400;
  line-height: normal;
  margin: 0 auto;
  width: 172px;
  height: 53px;
  flex-shrink: 0;
  border-radius: 4px;
  background: linear-gradient(
    270deg,
    #903aff 0%,
    #d434fe 56.42%,
    #ff26b9 99.99%,
    #fe34b9 100%
  );
  outline: none;
  border: none;
  cursor: pointer;
  display: flex;
  justify-content: center;
  align-items: center;
}
.contact__form__submit-button:disabled {
  cursor: not-allowed;
}
@media (max-width: 1400px) {
  .contact__main {
    padding: 30px;
  }
  .contact__info {
    width: 40%;
  }
  .contact__info img {
    object-fit: cover;
  }
}
@media (max-width: 1100px) {
  .contact__main__wrapper__bg__blur {
    padding-top: 145px;
  }
  .contact__main {
    min-height: calc(100vh - 145px);
  }
  .contact__main {
    flex-direction: column;
    align-items: center;
    width: 100%;
    max-width: 700px;
    margin: 0 auto;
  }
  .contact__form__title {
    display: block;
  }
  .contact__form {
    width: 100%;
    padding: 0px;
    background-color: none;
    background: rgba(255, 255, 255, 0);
    box-shadow: none;
  }
  .contact__info {
    max-width: 500px;
    width: 100%;
    height: auto;
    display: none;
  }
  .contact__info__section__share-on-wrapper--pos-bottom {
    display: flex;
  }
}
@media (max-width: 911px) {
  .contact__main__wrapper__bg__blur {
    padding-top: 105px;
  }

  .contact__main {
    min-height: calc(100vh - 105px);
  }
}
@media (max-width: 600px) {
  .contact__main__wrapper__bg__blur {
    padding-top: 65px;
  }
  .contact__main {
    min-height: calc(100vh - 65px);
    padding-top: 80px;
  }
}

.pop-enter-active,
.pop-leave-active {
  transition: transform 0.3s ease-in-out;
}
.pop-enter,
.pop-leave-to {
  transform: scale(0);
}
.pop-element {
  width: 100px;
  height: 100px;
  background-color: #3498db;
  color: white;
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>
