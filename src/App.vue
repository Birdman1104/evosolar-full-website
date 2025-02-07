<template>
  <div id="app">
    <Header />
    <Services />
    <BlocksSection />
    <OfferSection />
  </div>
</template>

<script>
import Header from './components/HeaderComponent.vue';
import Services from './components/ServicesComponent.vue';
import BlocksSection from './components/BlocksSection.vue';
import OfferSection from './components/OfferSection.vue';

export default {
  components: {
    Header,
    Services,
    BlocksSection,
    OfferSection,
  },
};
</script>

<style>
/* Global styles */
body {
  margin: 0;
  font-family: Arial, sans-serif;
}
</style>