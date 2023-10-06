<template>
  <div class="testimonial-slider">
    <div class="header-slider-title">
      <h1 v-html="title"></h1>
      <p v-html="subtitle"></p>
    </div>
    <div v-for="(testimonial, index) in testimonials" :key="index" class="testimonial">
      <div class="testimonial-info">
        <div class="testimonial-row">
          <img :src="testimonial.companyLogo" alt="Company Logo" class="company-logo" />
          <div class="testimonial-text">{{ testimonial.text }}</div>
        </div>
        <div class="testimonial-author">
          <div class="author-info">
            <div class="author-column">
              <div class="author-name">{{ testimonial.authorName }}</div>
              <div class="author-position">{{ testimonial.authorPosition }}</div>
            </div>
            <img :src="testimonial.authorImage" alt="Testimonial Author Image" class="testimonial-author-image" />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    title: String,
    subtitle: String,
  },
  data() {
    return {
      testimonials: [
        {
          companyLogo: require('@/assets/slider/bizhare.webp'),
          text: 'Kami sudah beberapa kali menggunakan jasa CyberArmy, kami selalu puas dengan hasil yang diberikan. Mulai dari tim yang profesional sampai kepada penyajian report hasil temuan yang cukup detail dan cepat. Sukses untuk CyberArmy, very recommended!',
          authorName: 'Giovanni Umboh',
          authorPosition: 'Co-founder and CTO Bizhare',
          authorImage: require('@/assets/testimony.png'),
        },
      ],
    };
  },
};
</script>

<style scoped>
.header-slider-title {
  display: flex;
  flex-direction: column;
  align-items: center;
  overflow: hidden;
  margin-bottom: 20px;
  margin-top: -50px;
  text-align: center;
}

.testimonial-slider {
  margin-left: 100px;
  margin-right: 100px;
  height: 400px;
  margin-bottom: 300px;
}

.testimonial-slider .testimonial {
  background-color: #ffffff;
  color: #000;
  font-family: sans-serif;
  font-size: 1.5rem;
  text-align: center;
  padding: 20px;
  border-radius: 10px;
  box-shadow: 0px 4px 6px rgba(0, 0, 0, 0.1); 
  transition: 0.5s;
  border-radius: 30px;
  margin-bottom: 100px;
}

.testimonial-slider .header-slider-title h1 {
  font-family: 'RobotoBold', sans-serif;
  font-size: 25px;
  font-weight: 700;
  margin-top: 130px;
  text-align: center;
  color: #000;
  margin-bottom: 10px;
}

.testimonial-slider .header-slider-title p {
  margin-top: 0px;
}
.testimonial-row {
  display: flex;
  flex-direction: row;
  align-items: center;
  padding: 40px;
}

.testimonial-row .company-logo {
  width: 250px;
  height: 50px;
}

.testimonial-author-image {
  width: 65px;
  height: 65px;
  border-radius: 100px;
  margin-left: 100px;
  margin-top: -15px;
}

.testimonial-text {
  font-size: 14.5px;
  text-align: left;
  padding: 10px;
  margin-left: 20px;
}

.testimonial-author {
  display: flex;
  flex-direction: row; 
  justify-content: flex-end; 
  text-align: right;
  margin: 20px;
}

.author-info {
  display: flex;
  flex-direction: row;
  margin-right: 10px;
}

.author-column {
  display: flex;
  flex-direction: column;
}

.author-name {
  font-size: 16px;
  font-weight: bold;
  text-align: left;
  color: #033c96;
}

.author-position {
  font-size: 14px;
  text-align: right;
  line-height: 30px;
  color: grey;
}
</style>
