<template>
  <div id="app">
    <b-container>
      <b-row>
        <Header/>
        <Footer/>
        <Breadcrumb :key="$route.fullPath" />
        
      </b-row>
      <b-row>
        <b-col cols="3"><LeftMenu /></b-col>
        <b-col cols="9">
          <router-view :key="$route.fullPath"></router-view>
        </b-col>
      </b-row>
    </b-container>
  </div>
</template>
<script>
import Header from "./components/Header.vue"
import Footer from "./components/Footer.vue"
import LeftMenu from "./components/LeftMenu.vue"
import Breadcrumb from "./components/Breadcrumb.vue"

export default {
  name: 'App',
  components: {
    Header,
    Footer,
    LeftMenu,
    Breadcrumb,
  }
}
</script>

<style>

</style>
