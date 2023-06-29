<script>
import AppFooter from './components/AppFooter.vue';
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import AppJumbotron from './components/AppJumbotron.vue';
export default{ components: { AppFooter, AppMain,AppJumbotron, AppHeader } }

</script>

<template>
  <div class="container">
    <AppHeader/>
    <AppMain/>
    <AppJumbotron/>
    <AppFooter/>
  </div>
</template>

<style>
.container{
  max-width: 1080px;
  margin: 0 auto;
}
</style>
