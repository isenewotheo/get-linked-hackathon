<template>
  <footer class="">
    <div class="footer__wrapper container">
      <section class="footer__first__section">
        <div class="footer__first__section__header">get<span>linked</span></div>
        <div class="footer__first__section__content">
          Getlinked Tech Hackathon is a technology innovation program <br />
          established by a group of organizations with the aim of showcasing
          <br />
          young and talented individuals in the field of technology
        </div>
        <div class="footer__first__section__terms">
          <div>Terms of Use</div>
          <div>Privacy Policy</div>
        </div>
      </section>
      <section class="footer__second__section">
        <div class="footer__second__section__header">Useful Links</div>
        <ul class="footer__second__section__content">
          <li>Overview</li>
          <li>Timeline</li>
          <li>FAQs</li>
          <li>Register</li>
        </ul>
        <div class="footer__second__section__follow-us">
          Follow us
          <div class="footer__second__section__follow-us__icons">
            <img src="@/assets/images/instagram.svg" alt="" />
            <img src="@/assets/images/X.svg" alt="" />
            <img src="@/assets/images/facebook.svg" alt="" />
            <img src="@/assets/images/linkedin.svg" alt="" />
          </div>
        </div>
      </section>
      <section class="footer__third__section">
        <div class="footer__third__section__header">Contact Us</div>
        <ul class="footer__third__section__content">
          <li>
            <img src="@/assets/images/footer-phone-icon.svg" alt="" />
            +234 6707653444
          </li>
          <li>
            <img src="@/assets/images/footer-location-icon.svg" alt="" />
            27,Alara Street <br />
            Yaba 100012 <br />
            Lagos State <br />
          </li>
        </ul>
      </section>
    </div>
    <div class="footer__copyright-info">
      All rights reserved. © getlinked Ltd.
    </div>
  </footer>
</template>

<script>
export default {};
</script>

<style scoped>
footer {
  background: #100b20;
  padding: 83px 20px;
  font-size: 12px;

  background-position: 70px 50px, 90px 100%, 86% 549px;
  background-image: url(@/assets/images/register-form-gradient-star.svg),
    url(@/assets/images/register-form-star-lightgrey.svg),
    url(@/assets/images/register-form-purple-star.svg);
  background-blend-mode: hard-light;
  background-repeat: no-repeat;
}
.footer__wrapper {
  display: flex;
  justify-content: space-between;
  flex-wrap: wrap;
}
.footer__first__section__header {
  font-family: Clash Display;
  font-size: 30px;
  font-style: normal;
  font-weight: 700;
  line-height: normal;
  color: #fff;
}
.footer__first__section__header span {
  color: #d434fe;
}
.footer__first__section__content {
  line-height: 20.688px;
  margin-bottom: 82px;
  margin-top: 16px;
}
.footer__first__section__terms {
  display: flex;
}
.footer__first__section__terms div {
  cursor: pointer;
}
.footer__first__section__terms :nth-child(2) {
  margin-left: 13px;
  padding-left: 13px;
  border-left: 2px solid #d434fe;
}
.footer__second__section__header,
.footer__third__section__header {
  color: #d434fe;
  font-family: Montserrat;
  font-size: 14px;
  font-style: normal;
  font-weight: 600;
  line-height: 172.4%; /* 24.136px */
}

.footer__second__section__content {
  display: flex;
  flex-direction: column;
  gap: 12px;
  margin: 12px 0;
}
.footer__second__section__content li {
  list-style: none;
  cursor: pointer;
}
.footer__second__section__follow-us {
  color: #d434fe;
  font-family: Montserrat;
  font-size: 12px;
  font-style: normal;
  font-weight: 400;
  line-height: normal;
  display: flex;
  align-items: center;
  gap: 16px;
}
.footer__second__section__follow-us__icons {
  /* margin-top: 14px; */
  display: flex;
  align-items: center;
  gap: 16.5px;
}
.footer__second__section__follow-us__icons img {
  cursor: pointer;
}
.footer__third__section__content {
  margin-top: 19px;
  display: flex;
  flex-direction: column;
  list-style-type: none;
  gap: 22px;
}
.footer__third__section__content li {
  display: flex;
  gap: 16px;
  line-height: 18.948px;
}
.footer__third__section__content li img {
  width: 15px;
}

.footer__copyright-info {
  margin: auto;
  margin-top: 53px;
  width: fit-content;
}

@media (max-width: 600px) {
  .footer__wrapper {
    cursor: pointer;
    gap: 32px;
  }
  .footer__first__section__content {
    line-height: 20.688px;
    margin-bottom: 39px;
    margin-top: 16px;
  }
}
</style>
