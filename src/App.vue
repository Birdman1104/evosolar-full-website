<template>
  <div id="app">
    <Header />
    <Services />
    <BlocksSection />
    <OfferSection />
    <CalculatorButton />
    <CasesSection />
    <CalculatorSection />
  </div>
</template>

<script>
import Header from './components/HeaderComponent.vue';
import Services from './components/ServicesComponent.vue';
import BlocksSection from './components/BlocksSection.vue';
import OfferSection from './components/OfferSection.vue';
import CalculatorButton from './components/CalculatorButton.vue';
import CasesSection from './components/CasesSection.vue';
import CalculatorSection from './components/CalculatorSection.vue';

export default {
  components: {
    Header,
    Services,
    BlocksSection,
    OfferSection,
    CalculatorButton,
    CalculatorSection,
    CasesSection,
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