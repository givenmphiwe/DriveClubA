<template>
  <div class="LearnPage">
    <img class="Image" src="../assets/car-large.jpg" />

    <div class="NewRange">New Range</div>
    <div class="LaFerr">LA FERRARI</div>
    <div class="lorem">Lorem ipsum dolor sit amet consectetur adipisicing elit. Mollitia placeat nam ipsa, deleniti quam asperiores est, voluptatibus nulla non molestias natus dolorem minus cumque inventore perspiciatis sed nemo! Ad, saepe! Loe
        <br>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Voluptas, ullam quia! Quod hic repudiandae accusamus velit voluptatum repellendus sit harum consequatur vitae pariatur tempore, incidunt esse. Reprehenderit earum veniam natus?
        <br><br>
        Lorem ipsum dolor, sit amet consectetur adipisicing elit. Autem in, architecto consectetur id atque quis eius praesentium neque dolore voluptatibus beatae harum, eum laboriosam laudantium quae recusandae, aperiam omnis suscipit?
        Lorem ipsum dolor sit amet consectetur adipisicing elit.
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
@import url("https://fonts.googleapis.com/css2?family=Poppins:wght@700&display=swap");

.LearnPage {
  background: #171b1e;
  width: 1440px;
  height: 820px;

  img {
    width: 810px;
    height: 820px;
    background: #161b1e 0% 0% no-repeat padding-box;
  }

  .NewRange {
    position: absolute;
    top: 90px;
    left: 890px;
    height: 21px;
    text-align: left;
    font: normal normal normal 18px/75px Proxima Nova;
    letter-spacing: 0.72px;
    color: #ffffff;
    text-transform: uppercase;
    opacity: 0.6;
  }

  .LaFerr {
    position: absolute;
    top: 121px;
    left: 890px;
    width: 325px;
    height: 64px;
    text-align: left;
    font: normal normal 800 56px/75px Proxima Nova;
    letter-spacing: 1.12px;
    color: #ffffff;
    text-transform: uppercase;
    opacity: 0.87;
  }

  .lorem {
    position: absolute;
    top: 245px;
    left: 890px;
    width: 470px;
    
    text-align: left;
    font: normal normal 300 18px/27px Poppins;
    letter-spacing: 0.36px;
    color: #ffffff;
    opacity: 0.87;
  }
}
</style>