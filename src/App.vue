<template>
  <div id="app">
    <navigation-bar class="item1"></navigation-bar>
    <page-header class="item2"></page-header>
    <div class="item3">
      <skill-container></skill-container>
      <contact-container></contact-container>
    </div>
    <page-footer class="item4"></page-footer>
  </div>
</template>

<script>
import SkillContainer from './components/SkillContainer.vue'
import PageHeader from './components/layout/PageHeader.vue'
import PageFooter from './components/layout/PageFooter.vue'
import NavigationBar from './components/ui/NavigationBar.vue'
import ContactContainer from './components/ContactContainer.vue'

export default {
  name: 'app',
  components: {
    SkillContainer,
    PageHeader,
    PageFooter,
    NavigationBar,
    ContactContainer
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
  grid-template-columns: auto;
  grid-template-rows: auto auto 1fr auto;
  grid-template-areas:
    'nav'
    'header'
    'main'
    'footer';
}
</style>
