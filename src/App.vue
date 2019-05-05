<template>
  <div id="app">
    <app-main-title/>
    <app-main-map />
  </div>
</template>

<script>
import MainTitle from './components/MainTitle.vue';
import MainMap from './components/MainMap.vue';

export default {
  name: 'app',
  components: {
    'app-main-title': MainTitle,
    'app-main-map': MainMap,
  },
}
</script>

<style>
@import './static/styles.css';
</style>
