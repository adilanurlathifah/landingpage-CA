<template>
<div class="navbar">
    <div class="logo-nav">
            <img :src="imageURL">
    </div>
    <nav>
        <ul>
            <li><router-link to="/program">Program</router-link></li>
            <li><router-link to="/produk">Produk</router-link></li>
            <li><router-link to="/tentang">Tentang</router-link></li>
        </ul>
    </nav>
    <button @click="masuk" class="masuk-button">Masuk</button>
    <button @click="daftar" class="daftar-button">Daftar</button>
</div>
</template>

<script>
export default {
    data() {
        return {
            imageURL: require('../assets/logo.png')
        }
    },
    methods: {
        masuk() {
            this.$router.push('/masuk')
        },
        daftar() {
            this.$router.push('/daftar')
        }
    }
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
    margin-top: -15px;
    z-index: 1000;
}

.navbar .logo-nav img {
  height: 44px;
  margin-top: 20px;
  margin-left: 140px;
}

.navbar nav ul {
    list-style-type: none;
    margin: 0;
    padding: 0;
}

.navbar nav li {
    display: inline-block;
    margin-left:20px;
    margin-right:-30px;
    margin-top: 5px;
}

.navbar nav a {
    font-weight: medium;
    color: #2c3e50;
    text-decoration: none;
    padding: 30px;
    font-size: 15px;
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
  margin-left: 400px;
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

</style>