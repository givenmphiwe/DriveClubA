<template>
  <div class="support">
    <Navigation />
    <img src="../assets/hero-home.jpg" />

    <div class="contact">CONTACT US</div>
    <div class="call">24/7 SUPPORT</div>
  </div>

  <div class="ContactData">

    <div class="ContactDetails">kdhjshkdfhjshkfh</div>
  
  </div>

  <div class="Empty"></div>

  <div type="footer">
    <Footer />
  </div>
</template>

<script>
// @ is an alias to /src
import Navigation from "../components/Navigation.vue";
import Footer from "../components/Footer.vue";
export default {
  name: "Contact",
  components: { Navigation, Footer },
};
</script>

<style lang="scss" scoped>
@import url("https://fonts.googleapis.com/css?family=Proxima+Nova");
@import url("https://fonts.googleapis.com/css2?family=Poppins:wght@700&display=swap");

.support {
  background-attachment: fixed;
  position: relative;
  width: 1438px;
  height: 398px;

  img {
    object-fit: cover;
    height: 100%;
    width: 100%;
  }

  .contact {
    position: absolute;
    top: 172px;
    left: 140px;
    width: 714px;
    height: 91px;
    font: normal normal 800 80px/75px Proxima Nova;
    letter-spacing: 1.6px;
    color: #ffffff;
  }

  .call {
    position: absolute;
    top: 259px;
    left: 140px;
    height: 45px;
    /* UI Properties */
    font: normal normal 800 40px/38px Proxima Nova;
    letter-spacing: 1.6px;
    color: #ffffff;
    text-transform: uppercase;
    opacity: 0.87;
    -webkit-text-stroke: 3px #fff;
  }
}
.ContactData {
  height: 430px;
  width: 1438px;
  background-color: #171b1e;
  border-bottom: 2px solid white;
  border-top: 2px solid white;

  .ContactDetails {
    position: absolute;
    background-color: #171b1e;
    border: 2px solid white;
    top: 322px;
    left: 732px;
    width: 588px;
    height: 738px;
  }
}

.Empty {
  height: 618px;
  width: 1438px;
  background-color: #171b1e;
  border-bottom: 2px solid white;
}
</style>
