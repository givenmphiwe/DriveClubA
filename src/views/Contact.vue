<template>
  <div class="support">
    <Navigation />
    <img src="../assets/hero-home.jpg" />

    <div class="contact">CONTACT US</div>
    <div class="call">24/7 SUPPORT</div>
  </div>

  <div class="ContactData">
    <div class="ContactIcon">
      <div class="PhoneIcon">
        <i class="fa fa-phone"></i>
      </div>

      <div class="SendIcon">
        <i class="fa fa-paper-plane" aria-hidden="true"></i>
      </div>

      <div class="LocationIcon">
        <i class="fa fa-map-marker" aria-hidden="true"></i>
      </div>
    </div>

    <div class="ContactDetails">
      <div class="heading">HOW CAN WE HELP YOU?</div>

      <div class="TextinputName">
        <label for="fname" class="Label">Name</label><br />
        <input type="text" class="Field" />
      </div>

      <div class="TextinputNumber">
        <label for="fname" class="Label">Contact number</label><br />
        <input type="text" class="Field" />
      </div>

      <div class="TextinputEmail">
        <label for="fname" class="Label">Email address</label><br />
        <input type="text" class="Field" />
      </div>

      <div class="TextinputHelp">
        <label for="fname" class="Label">How can we help you?</label><br />
        <textarea type="text" class="FieldText" />
      </div>

      <button type="button" class="SubmitBtn">Contact us</button>
    </div>
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
.ContactIcon {
  margin-top: 102px;
  margin-left: 140px;
  width: 264px;
  height: 228px;

  .PhoneIcon {
    width: 48px;
    height: 48px;
    border: 2px solid #ff0050;
    background: #ff00504d 0% 0% no-repeat padding-box;
    border: 2px solid #ff0050;
    opacity: 1;
  }

  .SendIcon {
    margin-top: 40px;
    width: 48px;
    height: 48px;
    border: 2px solid #ff0050;
    background: #ff00504d 0% 0% no-repeat padding-box;
    border: 2px solid #ff0050;
    opacity: 1;
  }

  .LocationIcon {
    margin-top: 40px;
    width: 48px;
    height: 48px;
    border: 2px solid #ff0050;
    background: #ff00504d 0% 0% no-repeat padding-box;
    border: 2px solid #ff0050;
    opacity: 1;
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
    height: 748px;

    .heading {
      margin-top: 60px;
      margin-left: 40px;
      height: 36px;
      text-align: left;
      font: normal normal bold 32px/38px Proxima Nova;
      letter-spacing: 1.28px;
      color: #ffffff;
      text-transform: uppercase;
      opacity: 0.87;
    }
    .TextinputName {
      margin-top: 24px;
    }
    .TextinputNumber {
      margin-top: 38px;
    }
    .TextinputEmail {
      margin-top: 38px;
    }
    .TextinputHelp {
      margin-top: 38px;
    }

    .Label {
      margin-left: 40px;
      width: 43px;
      height: 18px;
      text-align: left;
      font: normal normal medium 14px/18px Montserrat;
      letter-spacing: 0px;
      color: #ffffff;
      opacity: 0.87;
    }

    .Field {
      margin-top: 4px;
      margin-left: 41px;
      width: 507px;
      height: 50px;
      border: 1px solid #ffffffde;
      opacity: 0.87;
      background-color: #171b1e;
    }

    .FieldText {
      margin-top: 4px;
      margin-left: 41px;
      width: 507px;
      height: 172px;
      background: var(--black-high-) 0% 0% no-repeat padding-box;
      background: #171b1e 0% 0% no-repeat padding-box;
      border: 1px solid #ffffff;
      opacity: 1;
    }

    .SubmitBtn {
      margin-top: 32px;
      margin-left: 40px;
      width: 156px;
      height: 48px;
      background: #ff00504d 0% 0% no-repeat padding-box;
      border: 2px solid #ff0050;
    }
  }
}

.Empty {
  height: 618px;
  width: 1438px;
  background-color: #171b1e;
  border-bottom: 2px solid white;
}
</style>
