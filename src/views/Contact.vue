<template>
  
    <Navigation />
  <div v-show="!mobile" class="support">
    <img src="../assets/hero-home.jpg" />

    <div class="contact">CONTACT US</div>
    <div class="call">24/7 SUPPORT</div>
  </div>
  
  

  <!---Mobile--->
  <div v-show="mobile" class="Mobile-support">
    <img src="../assets/hero-home.jpg" />

    <div class="Mobile-contact">CONTACT US</div>
    <div class="Mobile-call">24/7 SUPPORT</div>
  </div>

  <div v-show="mobile" class="Mobile-ContactData">
    <div v-show="mobile" class="Mobile-ContactData">
     
    <div class="Mobile-ContactDetails">
      <div class="heading">HOW CAN WE HELP YOU?</div>

      <div class="TextinputName" data-error="Please try again">
        <label for="fname" class="Label">Name</label><br />
        <input type="text" class="Field" v-model="state.Name" />
        <span class="Err" v-if="v$.Name.$error">
          {{ v$.Name.$errors[0].$message }}
        </span>
      </div>

      <div class="TextinputNumber">

        <label for="fname" class="Label">Contact number</label><br />
        <input type="text" class="Field" v-model="state.number" />

        <span class="Err2" v-if="v$.number.$error">
          {{ v$.number.$errors[0].$message }}
        </span>
      </div>

      <div class="TextinputEmail">
        <label for="fname" class="Label">Email address</label><br />
        <input type="text" class="Field" v-model="state.email" />

        <span class="Err3" v-if="v$.email.$error">
          {{ v$.email.$errors[0].$message }}
        </span>
      </div>

      <div class="TextinputHelp">
        <label for="fname" class="Label">How can we help you?</label><br />
        <textarea type="text" class="FieldText" v-model="state.help" />
        
        <span class="Err4" v-if="v$.help.$error">
          {{ v$.help.$errors[0].$message }}
        </span>
      </div>

      <div class="triangleT"></div>
      <div class="triangleB"></div>
      
      <button type="button" @click="submitForm" class="SubmitBtn">
        Submit
      </button>

    </div>
    </div>
  </div>

  <div v-show="!mobile" class="ContactData">
    
    <div class="ContactIcon">
      <div class="PhoneIcon">
        <i
          class="fa fa-phone fa-rotate-90"
          style="color: #ffffff; margin: 15px 15px 15px 15px"
        ></i>
        <div class="triangleB"></div>
        <div class="triangleT"></div>
      </div>

      <div class="details">
        <p class="d">Phone</p>
        <p class="N">082 000 0000</p>

        <p class="d">Email</p>
        <p class="N">email@example.com</p>

        <p class="d">Location</p>
        <p class="N">42 Business RD</p>
      </div>

      <div class="SendIcon">
        <i
          class="fa fa-paper-plane"
          style="color: #ffffff; margin: 15px 15px 15px 15px"
        ></i>
        <div class="triangleB"></div>
        <div class="triangleT"></div>
      </div>

      <div class="LocationIcon">
        <i
          class="fa fa-map-marker"
          style="color: #ffffff; margin: 15px 15px 15px 15px"
        ></i>
        <div class="triangleB"></div>
        <div class="triangleT"></div>
      </div>
    </div>

    <div class="ContactDetails">
      <div class="heading">HOW CAN WE HELP YOU?</div>

      <div class="TextinputName" data-error="Please try again">
        <label for="fname" class="Label">Name</label><br />
        <input type="text" class="Field" v-model="state.Name" />
        <span class="Err" v-if="v$.Name.$error">
          {{ v$.Name.$errors[0].$message }}
        </span>
      </div>

      <div class="TextinputNumber">

        <label for="fname" class="Label">Contact number</label><br />
        <input type="text" class="Field" v-model="state.number" />

        <span class="Err2" v-if="v$.number.$error">
          {{ v$.number.$errors[0].$message }}
        </span>
      </div>

      <div class="TextinputEmail">
        <label for="fname" class="Label">Email address</label><br />
        <input type="text" class="Field" v-model="state.email" />

        <span class="Err3" v-if="v$.email.$error">
          {{ v$.email.$errors[0].$message }}
        </span>
      </div>

      <div class="TextinputHelp">
        <label for="fname" class="Label">How can we help you?</label><br />
        <textarea type="text" class="FieldText" v-model="state.help" />
        
        <span class="Err4" v-if="v$.help.$error">
          {{ v$.help.$errors[0].$message }}
        </span>
      </div>

      <div class="triangleT"></div>
      <div class="triangleB"></div>
      
      <button type="button" @click="submitForm" class="SubmitBtn">
        Submit
      </button>

    </div>
  </div>

  <!----------->


  <div v-show="!mobile" class="Empty"></div>

  <div v-show="mobile" class="Mobile-Empty">
    <div class="Mobile-ContactIcon">
      <div class="PhoneIcon">
        <i
          class="fa fa-phone fa-rotate-90"
          style="color: #ffffff; margin: 15px 15px 15px 15px"
        ></i>
        <div class="triangleB"></div>
        <div class="triangleT"></div>
      </div>

      <div class="details">
        <p class="d">Phone</p>
        <p class="N">082 000 0000</p>

        <p class="d">Email</p>
        <p class="N">email@example.com</p>

        <p class="d">Location</p>
        <p class="N">42 Business RD</p>
      </div>

      <div class="SendIcon">
        <i
          class="fa fa-paper-plane"
          style="color: #ffffff; margin: 15px 15px 15px 15px"
        ></i>
        <div class="triangleB"></div>
        <div class="triangleT"></div>
      </div>

      <div class="LocationIcon">
        <i
          class="fa fa-map-marker"
          style="color: #ffffff; margin: 15px 15px 15px 15px"
        ></i>
        <div class="triangleB"></div>
        <div class="triangleT"></div>
      </div>
    </div>
  </div>
  

  <div type="footer">
    <Footer />
  </div>
</template>

<script>
// @ is an alias to /src
import Navigation from "../components/Navigation.vue";
import Footer from "../components/Footer.vue";

import useValidate from "@vuelidate/core";
import { required, email, helpers } from "@vuelidate/validators";
import { reactive, computed } from "vue";

export default {
  name: "Contact",
  components: { Navigation, Footer },

data() {
    return {
      scrolledNav: null,
      mobile: null,
      mobileNav: null,
      windowWidth: null,
    };
  },
  created() {
    window.addEventListener("resize", this.checkScreen);
    this.checkScreen;
  },
 
//Checking the empty input fields
  setup() {
    const state = reactive({
      Name: "",
      number: "",
      email: "",
      help: "",
    });

    const Err = (value) => value.includes("vue");

    const rules = computed(() => {
      return {
        Name: { required: helpers.withMessage("Please try again", Err) },
        email: {
          required, email, Err: helpers.withMessage("Please try again", Err),
        },
        number: { required: helpers.withMessage("Please try again", Err) },
        help: { required: helpers.withMessage("Please try again", Err) },
      };
    });

    const v$ = useValidate(rules, state);

    return { state, v$ };
  },

  methods: {
    submitForm() {
      this.v$.$validate(); // checks all inputs
    },
    toggleMobileNav() {
      this.mobileNav = !this.mobileNav;
    },

    updateScroll() {
      const scrollPosition = window.scrollY;
      if (scrollPosition > 50) {
        this.scrolledNav = true;
        return;
      }
      this.scrolledNav = false;
    },

    checkScreen() {
      this.windowWidth = window.innerWidth;
      if (this.windowWidth <= 750) {
        this.mobile = true;
        return;
      }
      this.mobile = false;
      this.mobileNav = false;
      return;
    },
  },
};
</script>

<style lang="scss" scoped>
@import url("https://fonts.googleapis.com/css?family=Proxima+Nova");
@import url("https://fonts.googleapis.com/css2?family=Poppins:wght@700&display=swap");
@import '@/views/MobileContact.scss';

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

  .details {
    position: absolute;
    left: 208px;
    top: 500px;
  }

  .d {
    width: 58px;
    height: 25px;
    text-align: left;
    font: normal normal medium 18px/21px Poppins;
    letter-spacing: 0.36px;
    color: #ffffff;
    opacity: 0.87;
    margin-bottom: 2px;
  }

  .N {
    height: 25px;
    text-align: left;
    font: normal normal 300 18px/21px Poppins;
    letter-spacing: 0.36px;
    color: #ffffff;
    opacity: 0.6;
    margin-bottom: 38px;
  }
  .PhoneIcon {
    width: 48px;
    height: 48px;
    border: 2px solid #ff0050;
    background: #ff00504d 0% 0% no-repeat padding-box;
    border: 2px solid #ff0050;
    opacity: 1;

    .triangleB {
      position: absolute;
      top: 537px;
      width: 11px;
      height: 11px;
      border-bottom: 11px solid #ff0050;
      border-right: 11px solid transparent;
    }

    .triangleT {
      position: absolute;
      top: 502px;
      left: 177px;
      width: 11px;
      height: 11px;
      border-top: 11px solid #ff0050;
      border-left: 11px solid transparent;
    }
  }

  .SendIcon {
    margin-top: 40px;
    width: 48px;
    height: 48px;
    border: 2px solid #ff0050;
    background: #ff00504d 0% 0% no-repeat padding-box;
    border: 2px solid #ff0050;
    opacity: 1;

    .triangleB {
      position: absolute;
      top: 625px;
      width: 11px;
      height: 11px;
      border-bottom: 11px solid #ff0050;
      border-right: 11px solid transparent;
    }

    .triangleT {
      position: absolute;
      top: 590px;
      left: 177px;
      width: 11px;
      height: 11px;
      border-top: 11px solid #ff0050;
      border-left: 11px solid transparent;
    }
  }

  .LocationIcon {
    margin-top: 40px;
    width: 48px;
    height: 48px;
    border: 2px solid #ff0050;
    background: #ff00504d 0% 0% no-repeat padding-box;
    border: 2px solid #ff0050;
    opacity: 1;

    .triangleB {
      position: absolute;
      top: 713px;
      width: 11px;
      height: 11px;
      border-bottom: 11px solid #ff0050;
      border-right: 11px solid transparent;
    }

    .triangleT {
      position: absolute;
      top: 678px;
      left: 177px;
      width: 11px;
      height: 11px;
      border-top: 11px solid #ff0050;
      border-left: 11px solid transparent;
    }
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
      margin-top: 16px;
    }
    .TextinputEmail {
      margin-top: 16px;
    }
    .TextinputHelp {
      margin-top: 16px;
    }

    .Label {
      margin-left: 40px;
      width: 43px;
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
      color: #fff;
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
    .Err {
      position: absolute;
      top: 182px;
      left: 40px;
      letter-spacing: 0.56px;
      font: normal normal 300 14px/38px Proxima Nova;
      //width: 104px;
      height: 16px;
      color: #ff4e00;
      opacity: 1;
    }

    .Err2 {
      position: absolute;
      top: 270px;
      left: 40px;
      letter-spacing: 0.56px;
      font: normal normal 300 14px/38px Proxima Nova;
      height: 16px;
      color: #ff4e00;
      opacity: 1;
    }
    .Err3 {
      position: absolute;
      top: 357px;
      left: 40px;
      letter-spacing: 0.56px;
      font: normal normal 300 14px/38px Proxima Nova;
      height: 16px;
      color: #ff4e00;
      opacity: 1;
    }
    .Err4 {
      position: absolute;
      top: 571px;
      left: 40px;
      letter-spacing: 0.56px;
      font: normal normal 300 14px/38px Proxima Nova;
      height: 16px;
      color: #ff4e00;
      opacity: 1;
    }

    .triangleB {
      position: absolute;
      top: 650px;
      left: 40px;
      width: 11px;
      height: 11px;
      border-bottom: 11px solid #ff0050;
      border-right: 11px solid transparent;
    }

    .triangleT {
      position: absolute;
      top: 615px;
      left: 185px;
      width: 11px;
      height: 11px;
      border-top: 11px solid #ff0050;
      border-left: 11px solid transparent;
    }

    .SubmitBtn {
      margin-top: 32px;
      margin-left: 40px;
      width: 156px;
      height: 48px;
      background: #ff00504d 0% 0% no-repeat padding-box;
      border: 2px solid #ff0050;
      text-align: center;
      font: normal normal medium 18px/21px Poppins;
      letter-spacing: 0.36px;
      color: #ffffff;
      opacity: 1;

      &:hover {
        background-color: #ff0050;
        cursor: pointer;
      }
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
