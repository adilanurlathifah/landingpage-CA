<template>
  <div class="header-container">
    <div class="bg-body">
      <img :src="imageURL" class="dots">
      <img :src="imageURL2" class="polygon">
    </div>
    <header>
      <div class="header-container-title">
        <h1 v-html="pageTitle"></h1>
        <p v-html="subtitle"></p>
        <CustomButton class="custom-button-blue" label="Mulai Sekarang" buttonType="blue"></CustomButton>
      </div>
      <div class="header-container-image">
        <img :src="headerImg || defaultImg" alt="Gambar Header" class="header-image">
      </div>
    </header>
  </div>
</template>

<script>
import CustomButton from '@/components/custom_button.vue';

export default {
  name: 'header',
  components: {
    CustomButton,
  },
  props: {
    headerImg: String,
    defaultImg: String,
    pageTitle: String,
    subtitle: String,
  },
  data() {
    return {
      defaultImg: require('../assets/default_img.png'),
      imageURL: require('../assets/bg_dots.svg'),
      imageURL2: require('../assets/bg_polygon.webp'),
    };
  },
};
</script>

<style>
* {
  box-sizing: border-box;
}
.header-container {
  position: relative;
  overflow: hidden;
}

.bg-body {
  display: flex;
  max-width: 100%;
  overflow: hidden;
}

.dots {
  position: absolute;
  top: 100px;
  left: 0px;
  width: 95%;
  z-index: -1;
}

.polygon {
  position: absolute;
  top: -20px;
  right: 0px;
  width: 80%;
  z-index: 0;
  overflow: hidden;
}

header {
  display: flex;
  flex-direction: row;
  text-align: left;
  margin-left: 40px;
  margin-top: 70px;
  height: 500px;
  z-index: 1;
}

.header-container-title {
  flex-direction: column;
  margin-top: 130px;
  margin-left: 90px;
}

.header-container-title h1 {
  font-family: 'RobotoBold', sans-serif;
  font-size: 30px;
  font-weight: 700;
  color: black;
  line-height: 45px;
}

.header-container-title p {
  margin-top: -5px;
  font-family: 'Roboto', sans-serif;
  font-size: 19px;
  font-weight: 400;
  color: black;
  line-height: 29px;
}

.header-container-image {
  display: flex;
  margin-top: 70px;
  flex-direction: row;
  position: inherit;
}

.header-container-image img {
  width: 85%;
  z-index: 0;
  margin-left: 50px;
}

.custom_button .custom-button-blue {
    background-color: #004ECB;
    color: white;
    border: 0.75px solid #004ECB;
    border-radius: 5px;
    padding: 12px 40px;
    cursor: pointer;
    font-size: 20px;
    box-shadow: 0 0 15px rgba(0,0,0,.15);
}


.custom_button .custom-button-blue:hover {
  background: #2070f2;
  color: white;
}
</style>