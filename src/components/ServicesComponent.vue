<template>
    <section id="services" class="services">
      <h2>Services</h2>
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
            title: 'Service 1',
            description: 'Description for service 1.',
            image: require('./../assets/images/service1.jpg'),
          },
          {
            title: 'Service 2',
            description: 'Description for service 2.',
            image: require('./../assets/images/service2.jpg'),
          },
          {
            title: 'Service 3',
            description: 'Description for service 3.',
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