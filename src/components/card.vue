<template>
  <div class="card">
    <h1 class="main-title">{{ mainTitle }}</h1>
    <div class="card-image">
      <img :src="image || defaultImg" alt="Gambar Header" class="header-image">
    </div>
    <h1 v-html="title"></h1>
    <p>{{ description }}</p>
  </div>
</template>

<script>
export default {
  name: 'Card',
  props: {
    image: String,
    defaultImg: String,
    mainTitle: String, 
    title: String,
    description: String,
  },
  data() {
    return {
      defaultImg: require('../assets/default_img.png'),
    };
  },
};
</script>

<style>
.card {
  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: center;
  width: 300px;
  height: 220px;
  border-radius: 10px;
  background-color: #fff;
  box-shadow: 0 0 2px rgba(0, 0, 0, 0.1);
  padding: 20px;
}

.main-title {
  font-size: 24px; 
  font-weight: 700;
  margin-bottom: 10px; 
}

.card h1 {
  font-size: 17px;
  font-weight: 700;
  margin-top: 10px;
}

.card-image img {
  width: 93%;
  margin-top: -20px;
  max-height: 100px;
}

.card p {
  margin-top: 0px;
  font-size: 12px;
}
</style>
  