
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
  <AppHeader />
  <RouterView />
  <AppMain />
  <AppFooter />
</template>

<style></style>