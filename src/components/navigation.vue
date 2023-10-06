<template>
    <div class="navbar">
      <div class="logo-nav">
        <img :src="imageURL" />
      </div>
      <nav>
        <ul>
          <li><router-link to="/program">Program</router-link></li>
          <li><router-link to="/produk">Produk</router-link></li>
          <li><router-link to="/tentang">Tentang</router-link></li>
        </ul>
      </nav>
      <div class="buttons-container">
        <language_selector />
        <button @click="masuk" class="masuk-button">Masuk</button>
        <button @click="daftar" class="daftar-button">Daftar</button>
      </div>
    </div>
  </template>

<script>
import Language_selector from '@/components/language_selector.vue';

export default {
    components: {
        Language_selector
    },
    data() {
        return {
            imageURL: require('../assets/logo.png')
        };
    },
    methods: {
        masuk() {
            this.$router.push('/masuk');
        },
        daftar() {
            this.$router.push('/daftar');
        }
    },
    components: { Language_selector }
}
</script>

<style>
.navbar {
  width: 100%;
  height: 80px;
  display: flex;
  justify-content: left;
  align-items: center;
  padding-block: 1rem;
  background-color: #ffffff;
  position: fixed;
  font-family: 'Roboto', sans-serif;
  text-align: center;
  color: #2c3e50;
  z-index: 1000;
}

.navbar .logo-nav img {
  height: 44px;
  margin-top: 2px;
  margin-left: 140px;
}

.navbar nav ul {
  list-style-type: none;
  margin: 0;
  padding: 0;
}

.navbar nav li {
  display: inline-block;
  margin-left: 20px;
  margin-top: 5px;
}

.navbar nav a {
  font-weight: medium;
  color: #2c3e50;
  text-decoration: none;
  padding: 17px;
  font-size: 16px;
}

.navbar nav a:hover {
  color: #004ECB;
}

.masuk-button {
  background-color: #ffffff;
  color: #004ECB;
  border: 0.75px solid #004ECB;
  border-radius: 5px;
  padding: 10px 20px;
  cursor: pointer;
  border-color: #004ECB;
  font-size: 15px;
  margin-top: 10px;
  margin-right: 20px;
  justify-content: right;
}

.masuk-button:hover {
  background: #004ECB;
  color: white;
}

.daftar-button {
  background-color: #004ECB;
  color: white;
  border: 0.75px solid #004ECB;
  border-radius: 5px;
  padding: 10px 20px;
  cursor: pointer;
  font-size: 15px;
  margin-top: 10px;
  justify-content: right;
}

.daftar-button:hover {
  background: #2070f2;
}

.buttons-container {
  display: flex;
  align-items: center;
  margin-left: 270px;
}

.language-selector {
  margin-top: 10px;
  margin-right: 30px; 
}
</style>