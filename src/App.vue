<template>
  <div id="app">
    <div class="bar-dx">
      <div class="first">
        <img src="./assets/svg/svg-4.svg" alt="">
      </div>
      <div class="second">
        <img src="./assets/svg/svg-6.svg" alt="">
      </div>
      
    </div>
   <Header :items="navbaritems"/>
   <Main />
   <Footer 
   :socialItems="socials"
   :mail="email"
   :tel="number"
   :address="addresses"/>
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
          url:"#home",
          active:true,
        },
        {
          name:"Pages",
          url:"#pages",
          active:false,
        },
        {
          name:"Portfolio",
          url:"#portfolio",
          active:false,
        },
        {
          name:"Blog",
          url:"#blog",
          active:false,
        },
        {
          name:"Shop",
          url:"#shop",
          active:false,
        },
        {
          name:"Elements",
          url:"#elements",
          active:false,
        }
      ],
      socials:[
        {
          class:"fa-twitter",
          url:"https://twitter.com"
        },
        {
          class:"fa-pinterest-p",
          url:"https://www.pinterest.it/"
        },
        {
          class:"fa-facebook-f",
          url:"https://www.facebook.com"
        },
        {
          class:"fa-linkedin-in",
          url:"https://it.linkedin.com/"
        },
      ],
      email:"maree.qcode@hotmail.com",
      number:"+44645 321 789",
      addresses:[
        {
          name:"Avenue d'Auderghem 10",
          url:"https://www.google.it/maps/place/Avenue+d'Auderghem+10,+1000+Bruxelles,+Belgio/@50.841726,4.3823365,17z/data=!3m1!4b1!4m5!3m4!1s0x47c3c4a18bc7d62f:0xb112fd8cbf26bdbf!8m2!3d50.8417226!4d4.3845252"
        },
        {
          name:"1040 Brussels, Belgium",
          url:"https://www.google.it/maps/place/Avenue+d'Auderghem+10,+1000+Bruxelles,+Belgio/@50.841726,4.3823365,17z/data=!3m1!4b1!4m5!3m4!1s0x47c3c4a18bc7d62f:0xb112fd8cbf26bdbf!8m2!3d50.8417226!4d4.3845252"
        }
        
        
      ]
    }
  }
}
</script>

<style lang="scss">
@import '~@fortawesome/fontawesome-free/css/all.min.css';
@import './style/variables';
@import './style/mixin';
#app{
  position:relative;
  .bar-dx{
    position:fixed;
    right:0px;
    top:20px;
    z-index:3;
    .first,
    .second{
      @include center;
      width:40px;
      height:40px;  
      margin-bottom:10px;
      img{
        width:80%;
      }
    }
    .first{
      padding:5px;
      background-color:#EE2852 ;
    }
    .second{
      padding:10px;
      background-color: white;
    }
  }
}
</style>
