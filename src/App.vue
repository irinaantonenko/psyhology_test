<template>
  <div>
    <main-page/>
    <projects-page/>
    <about-me-page/>
    <contact-page/>
  </div>
</template>

<script>
import MainPage from './components/MainPage.vue';
import ContactPage from './components/ContactPage.vue';
import ProjectsPage from './components/ProjectsPage.vue';
import AboutMePage from './components/AboutMePage.vue';
export default {
  name: 'App',
  components: {
    MainPage,
    ContactPage,
    ProjectsPage,
    AboutMePage
  }
}
</script>

<style>
</style>
