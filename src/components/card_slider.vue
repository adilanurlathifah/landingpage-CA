<template>
  <div class="card-slider">
    <div class="header-slider-title">
        <h1 v-html="title"></h1>
        <p v-html="subtitle"></p>
    </div>
    <div class="cards" :style="{ transform: `translateX(-${currentIndex * cardWidth}px)` }">
      <div class="card" v-for="(card, index) in cards" :key="index">
        <img :src="card.image" alt="Card Image" :style="{ marginTop: card.marginTop + 'px' }" />
      </div>
    </div>
  </div>
</template>
  
<script>
export default {
  name: 'card_slider',
  props: {
    title: String,
    subtitle: String,
  },
  data() {
    return {
      cards: [
        {
          id: 1,
          image: require('@/assets/slider/bhinneka.webp'),
          marginTop: 20,
        },
        {
          id: 2,
          image: require('@/assets/slider/bobobox.webp'),
        },
        {
          id: 3,
          image: require('@/assets/slider/bpjs.webp'),
          marginTop: 25,
        },
        {
          id: 4,
          image: require('@/assets/slider/bssn.webp'),
        },
        {
          id: 5,
          image: require('@/assets/slider/dewaweb.webp'),
        },
        {
          id: 6,
          image: require('@/assets/slider/indihome.webp'),
          marginTop: 20,
        },
        {
          id: 7,
          image: require('@/assets/slider/jds.webp'),
          marginTop: 20,
        },
      ],
      currentIndex: 0,
      cardWidth: 300 
    };
  },
  methods: {
    prevCard() {
    },
    nextCard() {
    }
  }
};
</script>
  
<style scoped>
  .card-slider {
    display: flex;
    flex-direction: column;
    align-items: center;
    margin-top: -20px;
    width: 100%;
    overflow: hidden;
  }

  .card-slider .header-slider-title {
    align-items: center;
    margin-bottom: 50px;
    line-height: 17px;
  }

  .header-slider-title h1 {
    font-family: 'RobotoBold', sans-serif;
    font-size: 25px;
    font-weight: 700;
    margin-top: 150px;
    text-align: center;
    color: #000;
    margin-bottom: 10px;
  }
  
  .cards {
    display: flex;
    transition: transform 0.3s ease;
  }
  
  .card {
    width: 110px; 
    height: 90px;
    margin-right: 20px;
    padding: 10px;

    border: 1px solid #ccc;
    border-radius: 10px;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  }

  .card img {
    max-width: 75%;
  }
</style>