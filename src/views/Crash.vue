<template>
  <section class="crash">
    <article class="crash__left">
      <section class="crash__chart"></section>
      <section class="crash__inventory">
        <Inventory />
      </section>
    </article>
    <article></article>
    <article></article>
  </section>
</template>

<script>
import Inventory from '@/components/Inventory.vue';

export default {
  name: 'Crash',
  components: {
    Inventory,
  },
};
</script>

<style lang="scss" scoped>
  .crash {
    height: 100%;
    display: grid;
    grid-template-columns: 23% 1fr 23%;
    grid-column-gap: 20px;
    transition: .3s;

    @media (min-width: 1440px) {
      grid-column-gap: 25px;
    }

    @media (min-width: 1920px) {
      grid-column-gap: 34px;
    }
  }

  .crash__left {
    display: grid;
    grid-template-rows: 140px 1fr;
    grid-row-gap: 20px;
    transition: .3s;

    @media (min-width: 1440px) {
      grid-template-rows: 200px 1fr;
    }

    @media (min-width: 1920px) {
      grid-template-rows: 250px 1fr;
      grid-row-gap: 25px;
    }
  }

  .crash__chart, .crash__inventory {
    @include border-radius;
    background: var(--Black100);
    display: flex;
    flex-direction: column;
  }

  article:not(:first-of-type) {
    @include border-radius;
    background: var(--Black100);
  }
</style>
