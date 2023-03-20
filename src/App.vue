
<script>

import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import AppFooter from './components/AppFooter.vue';
export default {
  name: 'App',
  components: { AppHeader, AppFooter, AppMain }
};
</script>

<template>
  <div class="d-flex flex-column justify-content-between  vh-100">

    <AppHeader />
    <RouterView />

    <AppFooter />
  </div>
</template>

<style></style>