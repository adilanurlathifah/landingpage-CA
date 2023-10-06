<template>
  <div class="container">
    <Header :headerImg="headerImg" :pageTitle="pageTitle" :subtitle="pageSubtitle" />
    <CardSlider :title="slideTitle" :subtitle="slideSub" />
    <aside class="contact">
      <Contact />
    </aside>
  </div>
  <div class="titleCard">
    <h1 v-html="cardTitle"></h1>
  </div>
  <div class="home-view">
    <Card
      :image="card1.image"
      :title="card1.title"
      :description="card1.description"
    />
    <Card
      :image="card2.image"
      :title="card2.title"
      :description="card2.description"
    />
    <Card
      :image="card3.image"
      :title="card3.title"
      :description="card3.description"
    />
  </div>
  <big_card_slider :title="testTitle" :subtitle="testSubtitle" />
    <div class="box-container">
    <Container_blue
      :imgBoxOne="imgBoxOne"
      :imgBoxTwo="imgBoxTwo"
      :imgBoxThree="imgBoxThree"
      :imgBoxFour="imgBoxFour"
      
      :box_one="box_one"
      :box_two="box_two"
      :box_three="box_three"
      :box_four="box_four"
    />
    </div>  
    <div class="titleCard">
      <h1 v-html="cardTitle1"></h1>
      <p v-html="cardSubtitle"></p>
    </div>
    <div class="home-platform">
      <Card
      class="card"
        :image="card4.image"
        :title="card4.title"
      />
      <Card
        :image="card5.image"
        :title="card5.title"
      />
      <Card
        :image="card6.image"
        :title="card6.title"
      />
      <Card
        :image="card7.image"
        :title="card7.title"
      />
    </div>
    <div class="box-container">
    <Container_blue_2
      :header_one="header_one"
      :header_two="header_two"
      :header_three="header_three"
      :header_four="header_four"
      :header_five="header_five"
      
      :box_one="box_five"
      :box_two="box_six"
      :box_three="box_seven"
      :box_four="box_eight"
      :box_five="box_nine"
    />
    </div>
    <ClientCard :title="clientTitle" :clients="clientLogos" />
    <CustomButton class="custom-button-blue" label="Mulai Sekarang" buttonType="white"></CustomButton>
    <Footer />
</template>

<script>
import navigation from '@/components/navigation.vue';
import Header from '@/components/header.vue';
import Contact from '@/components/contact.vue';
import CardSlider from '@/components/card_slider.vue';
import Card from '@/components/card.vue';
import big_card_slider from '@/components/big_card_slider.vue';
import Container_blue from '@/components/container_blue.vue';
import Container_blue_2 from '@/components/container_blue_2.vue';
import ClientCard from '@/components/client_card.vue'; 
import Footer from '@/components/footer.vue';

export default {
  name: 'HomeView',
  components: {
    navigation,
    Header,
    Contact,
    CardSlider,
    Card,
    big_card_slider,
    Container_blue,
    Container_blue_2,
    ClientCard,
    Footer
},
  data() {
    return {
      headerImg: require('@/assets/header_img.svg'),
      pageTitle: '#1 CROWDSOURCED CYBER <br> SECURITY PLATFORM IN INDONESIA',
      pageSubtitle: 'Uji Keamanan Aplikasi Bisnis Anda Bersama <br> Bughunter Terbaik di sini!',
      
      slideTitle: 'TELAH DIPERCAYA OLEH',
      slideSub: 'Klien dari berbagai Industri yang telah memiliki kepercayaan pada kami',
      
      cardTitle: 'SOLUSI PLATFORM CYBER SECURITY TERPERCAYA', 
      testTitle: 'SUCCESS STORIES',
      testSubtitle: 'Apa kata pelanggan kami',
      
      imgBoxOne: require('@/assets/icon-continuous.svg'),
      imgBoxTwo: require('@/assets/icon-list.svg'),
      imgBoxThree: require('@/assets/icon-chart.svg'),
      imgBoxFour: require('@/assets/icon-chart-down.svg'),

      box_one: 'Pengujian Keamanan<br>Berkesinambungan',
      box_two: 'Hasil temuan kerentanan<br>bervariatif',
      box_three: 'Kerentanan diperbaiki<br>dengan cepat',
      box_four: 'Mengurangi risiko dari<br>kerentanan',

      header_one: '970',
      box_five: 'Bughunter Terverifikasi dari<br>komunitas dan profesional',
      header_two: '< 4 jam',
      box_six: 'Bughunter Terverifikasi dari<br>komunitas dan profesional',
      header_three: '22 Menit',
      box_seven: 'Bughunter Terverifikasi dari<br>komunitas dan profesional',
      header_four: '1006',
      box_eight: 'Bughunter Terverifikasi dari<br>komunitas dan profesional',
      header_five: '100+',
      box_nine: 'Bughunter Terverifikasi dari<br>komunitas dan profesional',

      cardTitle1: 'PENGUJIAN KEAMANAN',
      cardSubtitle: 'Dapat dilakukan di berbagai macam platform',
      
      clientTitle: 'BUGHUNTER KAMI DIAKUI OLEH',
      clientLogos: [
        {
        logo: require('@/assets/client/adobe.webp'), 
          width: 60,
          height: 70,
        },
        {
          logo: require('@/assets/client/algolia.webp'), 
          width: 100,
          height: 30, 
        },
        {
          logo: require('@/assets/client/apple.webp'), 
          width: 90,
          height: 50, 
        },
        {
          logo: require('@/assets/client/asus.webp'), 
          width: 90,
          height: 25, 
        },
        {
          logo: require('@/assets/client/bookingcom.webp'),
          width: 100,
          height: 20, 
        },
        {
          logo: require('@/assets/client/boredpanda.webp'),
          width: 120,
          height: 35, 
        },
        {
          logo: require('@/assets/client/buzz-feed.webp'), 
          width: 100,
          height: 20, 
        },
        {
          logo: require('@/assets/client/directly.webp'),
          width: 100,
          height: 30, 
        },
        {
          logo: require('@/assets/client/discourse.webp'),
          width: 100,
          height: 30, 
        },
        {
          logo: require('@/assets/client/dropbox.webp'),
          width: 100,
          height: 30, 
        },
        {
          logo: require('@/assets/client/flickr.webp'), 
          width: 50,
          height: 50, 
        },
        {
          logo: require('@/assets/client/ford.webp'), 
          width: 100,
          height: 40,
        },
        {
          logo: require('@/assets/client/google.webp'), 
          width: 100,
          height: 35,
        },
        {
          logo: require('@/assets/client/groupon.webp'), 
          width: 110,
          height: 25, 
        },
        {
          logo: require('@/assets/client/imgur.webp'), 
          width: 80,
          height: 30, 
        },
        {
          logo: require('@/assets/client/infogram.webp'), 
          width: 100,
          height: 30, 
        },
      ],
      card1: {
        image: require('@/assets/icon-bbp.png'),
        title: 'Bug Bounty Program',
        description: 'Memastikan kerentanan ditemukan oleh Bughunter beretika dan mengapresiasi hasilnya',
      },
      card2: {
        image: require('@/assets/icon-cda.png'),
        title: 'Cyber Security Training',
        description: 'Pelatihan Cyber Security dan Information Security untuk Perusahaan dan Individu',
      },
      card3: {
        image: require('@/assets/icon-helium.png'),
        title: 'Automated Security Testing',
        description: 'Platform Vulnerability Assessment dan Pentest Tools berbasis Cloud',
      },
      card4: {
        image: require('@/assets/icon-web.svg'),
        title: 'Web Application',
      },
      card5: {
        image: require('@/assets/icon-android.svg'),
        title: 'Android App',
      },
      card6: {
        image: require('@/assets/icon-ios-app.svg'),
        title: 'iOS App',
      },
      card7: {
        image: require('@/assets/icon-api.svg'),
        title: 'Desktop App',
      },
    };
  },
  methods: {
    customButtonClick() {
      this.$router.push('/daftar');
    },
  },
};
</script>

<style>

.titleCard {
  text-align: center;
}

.titleCard h1 {
  font-family: 'RobotoBold', sans-serif;
  font-size: 25px;
  font-weight: 700;
  margin-top: 90px;
  text-align: center;
  color: #000;
  margin-bottom: 10px;
}

.home-view {
  width: 80%;
  display: flex;
  flex-direction: row;
  justify-content: space-evenly;
  flex-wrap: wrap;
  margin-top: 40px;
  margin-left: 120px;
  /* margin-right: 120px; */
}

.home-platform {
  display: flex;
  flex-direction: row;
  justify-content: space-evenly;
  flex-wrap: wrap;
  margin-top: 40px;
  margin-left: 180px;
  margin-right: 180px;
  margin-bottom: 140px;
  height: 100px;
}

.home-platform .card {
  width: 200px; 
  height: 150px;
  border-radius: 30px;
}

.home-platform img {
  height: 70px;
}

.titleCard .cardTitle1 {
  font-family: 'RobotoBold', sans-serif;
  font-size: 25px;
  font-weight: 700;
  margin-top: 90px;
  text-align: center;
  color: #000;
  margin-bottom: 10px;
}
</style>