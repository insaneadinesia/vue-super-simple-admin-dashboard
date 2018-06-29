<template>
  <div id="app">
    <Header />

    <main id="site-main" role="main">
      <div class="container-fluid container-full">
        <div class="row no-gutters">
          <div class="col-12 col-md-2">
            <Sidebar />
          </div>
          <div id="site-content" class="col-12 col-md-10">
            <transition name="page">
              <router-view></router-view>
            </transition>
            <Footer />
          </div>
        </div>
      </div>
    </main>
  </div>
</template>

<script>
import Header from './components/layout/Header.vue';
import Footer from './components/layout/Footer.vue';
import Sidebar from './components/layout/Sidebar.vue';

export default {
  components: {
    Header,
    Footer,
    Sidebar,
  },
};
</script>

<style lang="scss">
  @import './assets/css/app.scss';
</style>
