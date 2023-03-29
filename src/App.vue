<template>
  <div class="wrapper">
    <page-header></page-header>
    <page-nav></page-nav>
    <page-main></page-main>
    <page-aside></page-aside>
    <page-footer></page-footer>
  </div>
</template>

<script setup>
  import PageHeader from './layout/PageHeader.vue'
  import PageFooter from './layout/PageFooter.vue'
  import PageMain from './layout/PageMain.vue'
  import PageNav from './layout/PageNav.vue'
  import PageAside from './layout/PageAside.vue'
</script>

<style>
  body { 
      margin: 0; 
      padding: 0;
      font-family: 'Segoe UI', Tahoma, Verdana, sans-serif;
  }
  .wrapper { 
    display: grid;
    grid-template-rows: min-content min-content 1fr min-content;
    grid-template-columns: 75% 25%;
    height: calc(100vh - 1rem);
    padding: .5rem;
  }

  @media all and (max-width: 1000px) {
    .wrapper {
      grid-template-columns: 100%;
    }
    .wrapper > * {
      grid-column: 1 / -1
    }
  }

  .wrapper > * {
    padding: 1rem;
  }

  header {
    grid-column: 1 / 3;
    background-color: blue;
    color: white
  }
  nav a+a {
    margin-left: 1rem
  }
  nav {
    grid-column: 1 / 3;
    background-color: aquamarine;
  }
  main { 
    grid-column: 1 / 2;
    background-color: beige;
  }
  aside {
    grid-column: 2 / 3;
    background-color: gold;
  }
  footer {
    grid-column: 1 / 3;
    background-color: yellowgreen;
    text-align: center;
  }
</style>
