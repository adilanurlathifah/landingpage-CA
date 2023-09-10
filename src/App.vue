<template>
    <div id="app">
    <Navigation/>
    <router-view/>
    </div>
</template>

<script>
import Header from '@/layout/Header.vue';
import Navigation from '@/layout/Navigation.vue';


export default {
  name: 'App',
  components: {
    Header,
    Navigation,
  },
};
</script>

<style>
#app {
  font-family: 'Roboto', sans-serif;
  text-align: center;
  color: #2c3e50;
}
</style>
