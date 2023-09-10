<template>
  <div class="header-container">
    <div class="bg-body">
      <img :src="imageURL" class="dots">
      <img :src="imageURL2" class="polygon">
    </div>
    <header>
      <div class="header-container-title">
        <h1 v-html="title"></h1>
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
  name: 'Header',
  components: {
    CustomButton,
  },
  props: {
    headerImg: String,
    defaultImg: String,
    title: String,
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
  /* overflow: hidden; */
}

.dots {
  position: absolute;
  top: 100px;
  left: 0px;
  z-index: -1;
}

.polygon {
  position: absolute;
  top: 0px;
  right: 0px;
  width: 80%;
  z-index: 0;
}

header {
  display: flex;
  flex-direction: row;
  text-align: left;
  margin-left: 40px;
  margin-top: 70px;
  z-index: 1;
}

.header-container-title {
  flex-direction: column;
  margin-top: 150px;
  margin-left: 100px;
}

.header-container-title h1 {
  font-family: 'RobotoBold', sans-serif;
  font-size: 28px;
  font-weight: 700;
  color: black;
  line-height: 45px;
}

.header-container-title p {
  margin-top: -5px;
  font-family: 'Roboto', sans-serif;
  font-size: 18px;
  font-weight: 400;
  color: black;
  line-height: 29px;
}

.header-container-image {
  margin-top: 90px;
}

.header-container-image img {
  z-index: 0;
}

.custom-button-blue {
  margin-top: 0px;
}
</style>