<template>
  <div>
    <Header :headerImg="headerImg" :title="pageTitle" :subtitle="pageSubtitle" />
  </div>
</template>

<script>
import Header from '@/layout/Header.vue';
import Navigation from '@/layout/Navigation.vue';

export default {
  name: 'HomeView',
  components: {
    Header,
  },
  data() {
    return {
      headerImg: require('@/assets/header_img.svg'), 
      pageTitle: '#1 CROWDSOURCED CYBER SECURITY<br>PLATFORM IN INDONESIA',
      pageSubtitle: 'Uji Keamanan Aplikasi Bisnis Anda Bersama<br>Bughunter Terbaik di sini!',
    };
  },
  methods: {
    customButtonClick() {
      this.$router.push('/daftar');
    },
  }
};
</script>

<style>
</style>
