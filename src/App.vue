<template>
  <div id="app">
    <section class="main">
      <header class="header"></header>
      <div class="main__content">
        <router-view />
      </div>
    </section>
  </div>
</template>

<style lang="scss">
#app {
  flex: 1;
  overflow: hidden;
  display: flex;
  flex-direction: column;
}

.main {
  display: grid;
  grid-template-rows: auto 1fr;
  height: 100%;
  padding: 28px 24px;
  overflow: hidden;
}

.header {
  padding: 20px 10px;
}
</style>
