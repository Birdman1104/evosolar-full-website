<template>
  <section id="blocks" class="blocks">
    <div class="block" v-for="(block, index) in blocks" :key="index">
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
        { title: 'Block 1', text: 'Text for block 1.' },
        { title: 'Block 2', text: 'Text for block 2.' },
        { title: 'Block 3', text: 'Text for block 3.' },
        { title: 'Block 4', text: 'Text for block 4.' },
      ],
    };
  },
};
</script>

<style scoped>
.blocks {
  display: grid;
  grid-template-columns: repeat(12, 1fr);
  grid-template-rows: auto auto;
  gap: 10px;
  background: #04210c;
  padding: 20px;
}

.block:nth-child(4n-3),
.block:nth-child(4n) {
  grid-column: span 7;
}

.block:nth-child(4n-2),
.block:nth-child(4n-1) {
  grid-column: span 5;
}

.block {
  border: 5px solid #237878;
  padding: 20px;
  color: white;
}

.block:only-child,
.block:last-child:nth-child(4n-3) {
  grid-column: span 12;
}

@media (max-width: 768px) {
  .blocks {
    grid-template-columns: 1fr;
    grid-template-rows: repeat(4, auto);
  }

  .blocks .block {
    grid-column: span 12;
  }
}
</style>