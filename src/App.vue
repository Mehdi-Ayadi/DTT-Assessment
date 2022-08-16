<template>
  <div class="app">
    <Navbar />
    <router-view>
      <HouseDescription />
      <HouseForm />
      <About />
    </router-view>
  </div>
</template>

<script>
import Navbar from "./components/Navbar.vue"
import HouseDescription from "./views/HouseDescription.vue"
import About from "./views/About.vue"
import HouseForm from "./views/HouseForm.vue"

export default {
  name: "App",
  components: { Navbar, HouseDescription, About, HouseForm }
};
</script>

<style lang="scss">
@font-face {
  font-family: "Montserrat";
  src: local("Montserrat"),
    url(./assets/Fonts/Montserrat-Medium.ttf) format("truetype");
}

@font-face {
  font-family: "MontserratBold";
  src: local("MontserratBold"),
    url(./assets/Fonts/Montserrat-Bold.ttf) format("truetype");
}

@font-face {
  font-family: "MontserratSemiBold";
  src: local("MontserratSemiBold"),
    url(./assets/Fonts/Montserrat-SemiBold.ttf) format("truetype");
}

@font-face {
  font-family: "MontserratLight";
  src: local("MontserratLight"),
    url(./assets/Fonts/Montserrat-Light.ttf) format("truetype");
}

@font-face {
  font-family: "MontserratRegular";
  src: local("MontserratRegular"),
    url(./assets/Fonts/Montserrat-Regular.ttf) format("truetype");
}

* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
  font-family: "Raleway", sans-serif;
  font-weight: 400;
}
.app {
  min-height: 300vh;
  position: relative;
  background-color: #F6F6F6;
}
.container {
  padding: 0 20px;
  max-width: 1140px;
  margin: 0 auto;
}
</style>