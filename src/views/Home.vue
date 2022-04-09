<template>
  <div class="hero">
    <Navigation />
    <img src="../assets/hero-home.jpg" />

    <div class="goosebumps">GOOSEBUMPS</div>
    <div class="come">COME STANDARD</div>
    <div class="discover">
      Discover the benefits of DRIVECLUB Trade-in an get a free vehicle
      evaluation
    </div>

    <button type="button" class="Contact-btn">Contact us</button>
  </div>

  <div class="ferrari">
    <img src="../assets/car-1.jpg" />

    <div class="vertical-line"></div>

    <div class="La-fer">LA FERR</div>
    <div class="new">new range</div>
    <div class="La-fer2">LA FERRARI</div>
    <div class="learn">Learn more</div>
  </div>

  <div class="models">
    <img src="../assets/car-2.jpg" />

    <div class="vertical-line"></div>

    <div class="Model">MODEL</div>
    <div class="new">new range</div>
    <div class="models">MODEL S</div>
    <div class="learn">Learn more</div>
  </div>
</template>

<script>
// @ is an alias to /src
import Navigation from "../components/Navigation.vue";
export default {
  name: "Home",
  components: { Navigation },
};
</script>

<style lang="scss" scoped>
@import url("https://fonts.googleapis.com/css?family=Proxima+Nova");
.hero {
  background-attachment: fixed;
  position: relative;
  width: 1438px;
  height: 598px;

  img {
    object-fit: cover;
    height: 100%;
    width: 100%;
  }

  .goosebumps {
    position: absolute;
    top: 172px;
    left: 140px;
    width: 714px;
    height: 91px;
    font: normal normal 800 80px/75px Proxima Nova;
    letter-spacing: 1.6px;
    color: #ffffff;
  }

  .come {
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
  }

  .discover {
    position: absolute;
    top: 332px;
    left: 140px;
    width: 466px;
    height: 45px;
    text-align: left;
    font: normal normal 300 16px/22px Poppins;
    letter-spacing: 0.32px;
    color: #ffffff;
    opacity: 0.6;
  }
  .Contact-btn {
    position: absolute;
    top: 419px;
    left: 140px;
    width: 156px;
    height: 48px;
    /* UI Properties */
    background: #ff00504d 0% 0% no-repeat padding-box;
    border: 2px solid #ff0050;
    opacity: 1;
  }
}

.ferrari {
  margin-top: 2px;
  height: 501px;
  width: 1438px;
  background-color: #14171a;

  img {
    position: absolute;
    left: 630px;
    width: 810px;
    height: 501px;
    margin-left: 2px;
    /* UI Properties */
    background: #161b1e 0% 0% no-repeat padding-box;
    opacity: 0.4;
  }

  .La-fer {
    position: relative;
    top: 103px;
    left: 0.000034332275390625px;
    width: 630px;
    height: 112px;
    background: #14171a 0% 0% no-repeat padding-box;
    opacity: 1;
    font: normal normal 800 96px/75px Proxima Nova;
    letter-spacing: 5.12px;
  }

  .new {
    top: 189px;
    left: 140px;
    //width: 108px;
    height: 21px;
    text-align: left;
    font: normal normal normal 18px/75px Proxima Nova;
    letter-spacing: 0.72px;
    color: #ffffff;
    text-transform: uppercase;
    opacity: 0.6;
  }

  .La-fer2 {
    top: 208px;
    left: 140px;
    height: 64px;
    text-align: left;
    font: normal normal 800 56px/75px Proxima Nova;
    letter-spacing: 1.12px;
    color: #ffffff;
    text-transform: uppercase;
    opacity: 0.87;
  }

  .learn {
    position: absolute;
    top: 892px;
    left: 140px;
    width: 101px;
    height: 23px;
    color: var(--unnamed-color-ff0050);
    text-align: left;
    font: normal normal normal 16px/25px Poppins;
    letter-spacing: 0.64px;
    color: #ff0050;
    opacity: 1;
  }
  .vertical-line {
    position: absolute;
    left: 630px;
    border-left: 2px solid white;
    height: 500px;
  }
}

.models {
  margin-top: 2px;
  height: 501px;
  width: 1438px;
  background-color: #14171a;

  img {
    position: absolute;
    left: 0px;
    width: 810px;
    height: 501px;
    margin-left: 2px;
    /* UI Properties */
    background: #161b1e 0% 0% no-repeat padding-box;
    opacity: 0.4;
  }

  .Model {
    position: relative;
    top: 101px;
    margin-left: 812px;
    height: 112px;
    opacity: 1;
    font: normal normal 800 96px/75px Proxima Nova;
    letter-spacing: 5.12px;
  }

  .new {
    top: 187px;
    margin-left: 976px;
    //width: 108px;
    height: 21px;
    text-align: left;
    font: normal normal normal 18px/75px Proxima Nova;
    letter-spacing: 0.72px;
    color: #ffffff;
    text-transform: uppercase;
    opacity: 0.6;
  }

  .models {
    top: 208px;
    margin-left: 976px;
    width: 250px;
    height: 64px;
    font: normal normal 800 56px/75px Proxima Nova;
    letter-spacing: 1.12px;
    color: #ffffff;
    text-transform: uppercase;
  }

  .learn {
    top: 292.5px;
    margin-left: 976px;
    width: 101px;
    height: 23px;

    font: normal normal normal 16px/25px Poppins;
    letter-spacing: 0.64px;
    color: #ff0050;
    opacity: 1;
  }
  .vertical-line {
    position: absolute;
    left: 810px;
    border-left: 2px solid white;
    height: 500px;
  }
}
</style>
