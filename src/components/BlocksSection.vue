<template>
    <section id="blocks" class="blocks">
      <div class="block" v-for="(block, index) in blocks" :key="index" :class="block.class">
        <h3>{{ block.title }}</h3>
        <p>{{ block.text }}</p>
      </div>
    </section>
  </template>
  
  <script>
  export default {
    data() {
      return {
        blocks: [
          { title: 'Block 1', text: 'Text for block 1.', class: 'wide' },
          { title: 'Block 2', text: 'Text for block 2.', class: 'narrow' },
          { title: 'Block 3', text: 'Text for block 3.', class: 'wide' },
          { title: 'Block 4', text: 'Text for block 4.', class: 'narrow' },
        ],
      };
    },
  };
  </script>
  
  <style scoped>
  .blocks {
    display: grid;
    grid-template-columns: 1.5fr 1fr;
    grid-template-rows: auto auto;
    gap: 10px;
    background: #04210c;
    padding: 20px;
  }
  
  .block {
    border: 5px solid #237878;
    padding: 20px;
    color: white;
  }
  
  .block.wide {
    grid-column: span 1.5;
  }
  
  .block.narrow {
    grid-column: span 1;
  }
  
  @media (max-width: 768px) {
    .blocks {
      grid-template-columns: 1fr;
      grid-template-rows: repeat(4, auto);
    }
  
    .block.wide,
    .block.narrow {
      grid-column: span 1;
    }
  }
  </style>