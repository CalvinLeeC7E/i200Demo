<template>
  <div id="app">
    <top-nav></top-nav>
    <menu-nav></menu-nav>
    <tool-nav></tool-nav>
    <main-view></main-view>
    <footer-view></footer-view>
  </div>
</template>

<script>
  import TopNav from './components/TopNav.vue'
  import MenuNav from './components/MenuNav.vue'
  import ToolNav from './components/ToolNav.vue'
  import MainView from './components/MainView.vue'
  import FooterView from './components/FooterView.vue'


  export default {
    name: 'app',
    components: {TopNav, MenuNav, ToolNav, MainView, FooterView}
  }
</script>

<style>
</style>
