<template>
  <div class="register__main__wrapper">
    <div class="register__main__wrapper__bg__blur">
      <div class="register__main">
        <h3 class="register__form__heading--top">Register</h3>
        <div class="register__image">
          <img
            src="@/assets/images/3d-graphic-designer-showing-thumbs.png"
            alt=""
          />
        </div>
        <form class="register__form" @submit.prevent="register()">
          <h3 class="register__form__heading">Register</h3>
          <div class="register__form__subtitle">
            Be part of this movement!
            <div class="register__form__subtitle__line__wrapper">
              <div class="register__form__subtitle__line">
                <img
                  src="@/assets/images/be-part-of-this-movement-girl-walking.svg"
                  alt=""
                />
                <img
                  src="@/assets/images/be-part-of-this-movement-boy-walking.svg"
                  alt=""
                />
              </div>
            </div>
          </div>
          <div class="register__form__title">CREATE YOUR ACCOUNT</div>
          <div class="register__form__form-group">
            <div class="register__form__input-group">
              <div class="register__form__input-group__label__and__input">
                <label for="Teams-Name">Team’s Name</label>
                <input
                  name="Team's Name"
                  type="text"
                  placeholder="Enter the name of your group"
                  id="Teams-Name"
                  v-model="formData.team_name"
                />
              </div>
              <div class="register__form__input-group__label__and__input">
                <label for="Phone">Phone</label>
                <input
                  type="tel"
                  placeholder="Enter your phone number"
                  id="Phone"
                  name="Phone"
                  v-model="formData.phone_number"
                />
              </div>
            </div>
            <div class="register__form__input-group">
              <div class="register__form__input-group__label__and__input">
                <label for="Email">Email</label>
                <input
                  type="email"
                  placeholder="Enter your email address"
                  id="Email"
                  name="E-mail"
                  v-model="formData.email"
                />
              </div>
              <div class="register__form__input-group__label__and__input">
                <label for="Project-Topic">Project Topic</label>
                <input
                  type="text"
                  placeholder="What is your group project topic"
                  id="Project-Topic"
                  name="Project Topic"
                  v-model="formData.project_topic"
                />
              </div>
            </div>
            <div
              class="register__form__input-group register__form__input-group__selects"
            >
              <div
                class="register__form__input-group__label__and__input register__form__input-group__label__and__input__category"
              >
                <label for="Category">Category</label>
                <select
                  name="Category"
                  v-model="formData.category"
                  id="Category"
                >
                  <option :value="0">Select your category</option>
                  <option
                    :value="category.id"
                    v-for="(category, index) in categoriesList"
                    :key="index"
                  >
                    {{ category.name }}
                  </option>
                </select>
              </div>
              <div
                class="register__form__input-group__label__and__input register__form__input-group__label__and__input__group-size"
              >
                <label for="Group-Size">Group Size</label>
                <select
                  name="Group Size"
                  v-model="formData.group_size"
                  id="Group-Size"
                >
                  <option :value="0">Select</option>
                  <option :value="index" v-for="index in 10" :key="index">
                    {{ index }}
                  </option>
                </select>
              </div>
            </div>
          </div>
          <div class="register__form__info">
            Please review your registration details before submitting
          </div>
          <div class="register__form__terms-and-condition">
            <input
              type="checkbox"
              v-model="formData.privacy_poclicy_accepted"
            />
            I agreed with the event terms and conditions and privacy policy
          </div>
          <button
            :disabled="loading || !formIsValid"
            class="register__form__submit-button"
          >
            <div class="spinner" v-if="loading"></div>
            <span v-else
              ><span class="register__form__submit-button__text--long"
                >Register Now</span
              ><span class="register__form__submit-button__text--short"
                >Submit</span
              ></span
            >
          </button>
        </form>
      </div>
    </div>
    <RegistrationSuccessfulModal
      v-if="showRegSuccessful"
      @back="showRegSuccessful = false"
    />
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
        team_name: "",
        group_size: 0,
        project_topic: "",
        category: 0,
        privacy_poclicy_accepted: false,
      },
      loading: false,
      showRegSuccessful: false,
    };
  },
  computed: {
    formIsValid() {
      let k = this.formData;
      return (
        k.email !== "" &&
        k.phone_number !== "" &&
        k.team_name !== "" &&
        k.group_size > 0 &&
        k.category > 0 &&
        k.privacy_poclicy_accepted
      );
    },
  },
  async mounted() {
    try {
      let res = await fetch(`${this.baseUrl}/hackathon/categories-list`);
      let response = await res.json();
      this.categoriesList = response;
    } catch (error) {
      console.error(error);
    }
  },
  methods: {
    async register() {
      try {
        this.loading = true;
        let res = await fetch(`${this.baseUrl}/hackathon/registration`, {
          method: "POST",
          headers: {
            "Content-Type": "application/json",
          },
          body: JSON.stringify(this.formData),
        });
        let response = await res.json();
        if (!res.ok) {
          if (response.email) {
            alert(response.email);
          } else {
            throw new Error("Network response was not ok");
          }
        }
        this.showRegSuccessful = true;
      } catch (error) {
        console.error(error);
      } finally {
        this.loading = false;
      }
    },
  },
};
</script>

<style scoped>
.register__main__wrapper {
  background: #150e28;
  background-position: 0% 100px, 100% 100%;
  background-image: url(@/assets/images/Purple-Lens-Flare-PNG.png),
    url(@/assets/images/Purple-Lens-Flare-PNG.svg);
  background-blend-mode: hard-light;
  background-repeat: no-repeat;
  background-size: 760px 560px;
}
.register__main__wrapper__bg__blur {
  backdrop-filter: blur(80px);
  padding-top: 185px;
  /* padding-top: var(--header-height); */
}
.register__main {
  display: flex;
  flex-wrap: wrap;
  min-height: calc(100vh - 185px);
  align-items: flex-start;
  justify-content: center;
  /* padding: 10px 30px; */
  max-width: 1350px;
  margin: auto;

  background-position: right 100px top 755px;
  background-image: url(@/assets/images/register-form-small-star.svg);
  background-blend-mode: hard-light;
  background-repeat: no-repeat;
}
.register__image {
  width: 717px;
  height: 717px;
  /* background-color: green; */

  background-position: 70px 50px, 90px 100%, 86% 549px;
  background-image: url(@/assets/images/register-form-gradient-star.svg),
    url(@/assets/images/register-form-star-lightgrey.svg),
    url(@/assets/images/register-form-purple-star.svg);
  background-blend-mode: hard-light;
  background-repeat: no-repeat;
}
.register__image img {
  width: 100%;
  height: 100%;
}
.register__form {
  max-width: 740px;
  flex: 1;
  padding: 65px 91px;
  border-radius: 12px;
  background: rgba(255, 255, 255, 0.03);
  box-shadow: 0px 4px 4px 0px rgba(0, 0, 0, 0.25);
  background-position: 70% 18px;
  background-image: url(@/assets/images/register-form-star-lightgrey.svg);
  background-blend-mode: hard-light;
  background-repeat: no-repeat;
}
.register__form__heading {
  color: #d434fe;
  font-family: "Clash Display";
  font-size: 32px;
  font-weight: 600;
  line-height: normal;
  margin-bottom: 46px;
}
.register__form__heading--top {
  display: none;
  color: #d434fe;
  font-family: "Clash Display";
  font-size: 22px;
  font-weight: 600;
  line-height: normal;
  margin-bottom: 46px;
  align-self: flex-start;
}
.register__form__subtitle {
  color: #fff;
  font-family: Montserrat;
  font-size: 14px;
  font-weight: 400;
  line-height: normal;
  margin-bottom: 19px;
  display: flex;
  align-items: baseline;
}
.register__form__subtitle__line__wrapper {
  padding-bottom: 3px;
}
.register__form__subtitle__line {
  border-bottom: 1px solid #d434fe;
  border-bottom-style: dashed;
  width: 101px;
  display: flex;
  justify-content: center;
}
.register__form__title {
  color: #fff;
  font-family: Montserrat;
  font-size: 24px;
  font-weight: 400;
  line-height: normal;
  margin-bottom: 33px;
}
.register__form__form-group {
  display: flex;
  flex-direction: column;
  gap: 29px;
  margin-bottom: 23px;
}
.register__form__input-group {
  /* margin: 20px 0; */
  display: grid;
  gap: 32px;
  grid-template-columns: repeat(auto-fill, minmax(min(200px, 263px), 1fr));
}
.register__form__input-group__label__and__input {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  height: 75px;
}
.register__form__input-group__label__and__input label {
  color: #fff;
  font-family: Montserrat;
  font-size: 14px;
  font-weight: 400;
  line-height: normal;
}
.register__form__input-group__label__and__input input,
.register__form__input-group__label__and__input select {
  color: #fff;
  height: 47px;
  border-radius: 4px;
  border: 1px solid #fff;
  background: rgba(255, 255, 255, 0.03);
  box-shadow: 0px 4px 4px 0px rgba(0, 0, 0, 0.25);
  padding: 15px 27px;
  outline: none;
}
.register__form__input-group__label__and__input select {
  appearance: none;
  background-repeat: no-repeat;
  background-position: right 13.5px center;
  background-image: url("@/assets/images/select-arrow-down.svg");
}
.register__form__input-group__label__and__input input::placeholder {
  color: rgba(255, 255, 255, 0.25);
}
.register__form__info {
  color: #ff26b9;
  font-family: Montserrat;
  font-size: 12px;
  font-style: italic;
  font-weight: 400;
  line-height: normal;
  margin-bottom: 16px;
}
.register__form__terms-and-condition {
  color: #fff;
  font-family: Montserrat;
  font-size: 12px;
  font-weight: 400;
  line-height: normal;
  margin-bottom: 22px;
  display: flex;
  align-items: center;
  gap: 10px;
}
.register__form__terms-and-condition input {
  background-color: none;
  width: 14px;
  height: 14px;
  flex-shrink: 0;
  display: block;
  appearance: none;
  -webkit-appearance: none;
  -moz-appearance: none;
  width: 20px;
  height: 19px;
  border: 2px solid white;
  border-radius: 3px;
  outline: none;
  cursor: pointer;
  position: relative;
}

.register__form__terms-and-condition input[type="checkbox"]:checked:before {
  content: "";
  position: absolute;
  top: 0px;
  left: 6px;
  width: 5px;
  height: 13px;
  border: solid white;
  border-width: 0 2px 2px 0;
  transform: rotate(45deg);
}
.register__form__submit-button {
  color: #fff;
  font-family: Montserrat;
  font-size: 16px;
  font-weight: 400;
  line-height: normal;
  width: 100%;
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
.register__form__submit-button:disabled {
  cursor: not-allowed;
}
.register__form__submit-button__text--short {
  display: none;
}
@media (max-width: 1400px) {
  .register__main {
    padding: 30px;
  }
  .register__image {
    width: 40%;
  }
  .register__image img {
    object-fit: cover;
  }
}
@media (max-width: 1100px) {
  .register__main__wrapper__bg__blur {
    padding-top: 145px;
  }
  .register__main {
    flex-direction: column;
    align-items: center;
    width: 100%;
    max-width: 700px;
    margin: 0 auto;
  }
  .register__form__heading {
    display: none;
  }
  .register__form__heading--top {
    display: block;
  }
  .register__form {
    width: 100%;
    padding: 0px;
    background-color: none;
    background: rgba(255, 255, 255, 0);
    box-shadow: none;
  }
  .register__image {
    max-width: 500px;
    width: 100%;
    height: auto;
  }
}
@media (max-width: 911px) {
  /* .register__form {
    padding: 0px;
  } */

  .register__main__wrapper__bg__blur {
    padding-top: 105px;
  }
  .register__form__input-group__selects {
    display: flex;
  }
  .register__form__input-group__label__and__input__group-size {
    width: 87px;
  }
  .register__form__input-group__label__and__input__category {
    width: auto;
    flex: 1;
  }
}
@media (max-width: 600px) {
  .register__main__wrapper__bg__blur {
    padding-top: 65px;
  }
  .register__form__title {
    font-size: 20px;
  }
  .register__form__submit-button__text--long {
    display: none;
  }
  .register__form__submit-button__text--short {
    display: inline;
  }
}
@media (max-width: 350px) {
  .register__form__input-group__selects {
    flex-direction: column;
  }
  .register__form__input-group__label__and__input__group-size {
    width: 100%;
  }
  .register__form__input-group__label__and__input__category {
    width: 100%;
  }
}
</style>
