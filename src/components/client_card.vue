<template>
  <div class="client-card">
    <h2>{{ title }}</h2>
    <div class="client-logos">
      <div v-for="(client, index) in clients" :key="index" class="client-logo">
        <img
          :src="client.logo"
          :alt="client.name"
          :style="{ width: client.width + 'px', height: client.height + 'px' }"
        />
      </div>
    </div>
    <div class="button-container">
      <button class="custom-button-white">Lihat Lebih Banyak</button>
    </div>
  </div>
</template>

<script>
import CustomButton from './custom_button.vue';

export default {
  name: 'ClientCard',
  props: {
    title: String,
    clients: Array,
  },
};
</script>

<style scoped>
.client-card {
  display: flex;
  flex-direction: column;
  background-color: #fff;
  padding: 20px;
  margin-top: 50px;
  margin-left: 100px;
  margin-right: 100px;
  border-radius: 10px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
}

.client-card h2 {
  font-family: 'RobotoBold', sans-serif;
  font-size: 26px;
  color: black;
  margin-top: 20px;
  margin-bottom: 20px;
}

.client-logos {
  display: flex;
  flex-wrap: wrap;
  justify-content: flex-start; 
  align-items: center;
  padding: 25px;
  gap: 20px;
}

.client-logo {
  max-width: 100%;
  width: auto;
  max-height: 200px;
  margin-bottom: 20px;
  margin-top: 0px;
  flex: 1; 
  text-align: center; 
}

.button-container {
  display: flex;
  justify-content: center;
  margin-top: 10px;
  z-index: 1;
}

button.custom-button-white {
  background-color: #ffffff;
  color: #004ecb;
  border: 0.75px solid #004ecb;
  border-radius: 10px;
  padding: 10px;
  cursor: pointer;
  margin-top: -30px;
  margin-bottom: 30px;
  border-color: #004ecb;
  font-size: 14px;
}

button.custom-button-white:hover {
  background: #4980d8;
  color: white;
}
</style>