<template>
  <section id="services" class="services">
    <h2>OUR SERVICES</h2>
    <p>We provide the best services for your needs.</p>
    <div class="service-cards">
      <div class="card" v-for="(service, index) in services" :key="index">
        <img :src="service.image" :alt="service.title" />
        <h3>{{ service.title }}</h3>
        <p>{{ service.description }}</p>
        <button @click="scrollToContact">Learn More</button>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      services: [
        {
          title: 'Design and Installation of Solar Systems',
          description: 'We offer premium solar system design and installation services for both homes and businesses, free of charge.',
          image: require('./../assets/images/service1.jpg'),
        },
        {
          title: 'Maintenance of Solar Systems',
          description: 'We provide maintenance services for both solar systems installed by us and those installed by other companies.',
          image: require('./../assets/images/service2.jpg'),
        },
        {
          title: 'Adding Solar Panels to Your Existing System',
          description: 'Increase the capacity of your existing solar system. We specialize in adding solar panels and expanding your system for improved energy efficiency.',
          image: require('./../assets/images/service3.jpg'),
        },
      ],
    };
  },
  methods: {
    scrollToContact() {
      // document.getElementById('contact').scrollIntoView({ behavior: 'smooth' });
    },
  },
};
</script>

<style scoped>
.services {
  background: white;
  padding: 50px 20px;
  text-align: center;
}

.service-cards {
  display: flex;
  justify-content: space-around;
  flex-wrap: wrap;
  gap: 20px;
}

.card {
  flex: 1 1 30%;
  max-width: 30%;
  text-align: center;
}

.card img {
  width: 100%;
  height: auto;
}

@media (max-width: 768px) {
  .card {
    flex: 1 1 100%;
    max-width: 100%;
  }
}
</style>