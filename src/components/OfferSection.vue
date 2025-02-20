<template>
  <section id="offer" class="offer">
    <h2>5 STEPS TO YOUR SOLAR SYSTEM</h2>
    <p>Explore our services and solutions.</p>
    <div class="circles">
      <div class="circle" v-for="(offer, index) in offers" :key="index">
        <div class="icon">{{ offer.icon }}</div>
        <h3>{{ offer.title }}</h3>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      offers: [
        { title: 'Consultation, Measurement', icon: '💡' },
        { title: 'Design', icon: '🎨' },
        { title: 'Preparation Work', icon: '📋' },
        { title: 'Installation', icon: '🔧' },
        { title: 'Monitoring', icon: '📊' },
      ],
    };
  },
};
</script>

<style scoped>
.offer {
  background: white;
  padding: 50px 20px;
  text-align: center;
}

.circles {
  display: flex;
  justify-content: space-around;
  align-items: center;
  position: relative;
}

.circles::before {
  content: '';
  position: absolute;
  top: 50%;
  left: 0;
  right: 0;
  height: 2px;
  background: black;
  z-index: 0;
}

.circle {
  position: relative;
  z-index: 1;
  background: white;
  border: 2px solid black;
  border-radius: 50%;
  width: 100px;
  height: 100px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.icon {
  font-size: 24px;
}

@media (max-width: 768px) {
  .circles {
    flex-direction: column;
  }

  .circles::before {
    top: 0;
    left: 50%;
    width: 2px;
    height: 100%;
  }
}
</style>