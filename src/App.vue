<template>
  <div id="app">
   <Header :items="navbaritems"/>
   <Main />
   <Footer />
  </div>
</template>

<script>
import Header from './components/Header.vue';
import Main from './components/Main.vue';
import Footer from './components/Footer.vue';

export default {
  name: 'App',
  components: {
    Header,
    Main,
    Footer
  },
  data(){
    return {
      navbaritems:[
        {
          name:"Home",
          url:"#Home",
          active:false,
        },
        {
          name:"Pages",
          url:"#Pages",
          active:false,
        },
        {
          name:"Portfolio",
          url:"#Portfolio",
          active:false,
        },
        {
          name:"Blog",
          url:"#Blog",
          active:false,
        },
        {
          name:"Shop",
          url:"#Shop",
          active:false,
        },
        {
          name:"Elements",
          url:"#Elements",
          active:false,
        }
      ]
    }
  }
}
</script>

<style lang="scss">
@import '~@fortawesome/fontawesome-free/css/all.min.css';
@import './style/variables';
</style>
