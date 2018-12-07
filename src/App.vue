<template>
  <div id="app">
    <navigation-bar class="item1"></navigation-bar>
    <page-header class="item2"></page-header>
    <skill-body class="item3"></skill-body>
    <page-footer class="item4"></page-footer>
  </div>
</template>

<script>
import SkillBody from './components/SkillBody.vue'
import PageHeader from './components/layout/PageHeader.vue'
import PageFooter from './components/layout/PageFooter.vue'
import NavigationBar from './components/ui/NavigationBar.vue'

export default {
  name: 'app',
  components: {
    SkillBody,
    PageHeader,
    PageFooter,
    NavigationBar
  }
}
</script>

<style>
html, body {
    margin: 0px;
    height: 100%;
    width: 100%;
    font-family: 'Avenir', Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
}

.text-uppercase {
    text-transform: uppercase;
}

.item1 { grid-area: nav; }
.item2 { grid-area: header; }
.item3 { grid-area: main; }
.item4 { grid-area: footer; }

#app {
  display: grid;
  height: 100%;
  grid-template-columns: 20% auto 20%;
  grid-template-rows: auto auto 1fr auto;
  grid-template-areas:
    'nav nav nav'
    'header header header'
    'main main main'
    'footer footer footer';
}
</style>
