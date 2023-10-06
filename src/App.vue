<template>
  <div id="app">
  <Navigation/>
  <router-view/>
  </div>
</template>

<script>
import Header from './components/header.vue';
import Navigation from '@/components/navigation.vue';

export default {
name: 'app',
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