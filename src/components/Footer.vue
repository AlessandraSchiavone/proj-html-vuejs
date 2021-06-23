<template>
  <footer>
      <div class="box">
            <div class="logo col-lg-3">
                <img src="../assets/img/logo-sidearea-1.png" alt="">
                <h5>Let's Get Creative</h5>   
            </div>
            <div class="col-lg-3">
                <h6>
                    {{ mail }}
                </h6>
                <h6>
                   {{ tel }}
                </h6>
            </div>
            <div class="col-lg-3">
                <h6 v-for="item,index in address" :key="index">
                    <a :href="item.url"
                        target="_blank">
                         {{ item.name }} 
                    </a>
                </h6>   
            </div>
            <div class="col-lg-3">
                <h6>Stay in touch with us</h6>
                <ul>
                    <li v-for="(item,index) in socialItems" :key="index">
                        <a :href="item.url"
                            target="_blank" >
                            <i class="fab" :class="item.class"></i>
                        </a>
                    </li>
                </ul>
            </div>   
      </div>
      <div class="chevron-up">
          <a href="/">
              <img src="../assets/svg/svg-2.svg" alt="Up">
          </a>    
      </div>    
  </footer>
</template>

<script>
export default {
    name:"Footer",
    props:{
        socialItems: Array,
        mail: String,
        tel: String,
        address: Array   
        }
}
</script>

<style lang="scss" scoped>
@import '../style/mixin';
@import "../style/variables";
footer{
    position:relative;
    height:250px;
    background-color:#C0E1CF;
    .box{
       @include center;
       height:100%;
       width:70%;
       margin: 0 auto;
       .col-lg-3{
           margin:0px 30px;
       }
       .logo{
           @include center;
           flex-direction: column;
           img{
               width:40%;
           }
           h5{
              font-size:18px;
              font-weight:300;
              margin: 20px 0;
           }
       }
       a{   
           cursor:pointer;
           text-decoration: none;
            color:black;
        }
       ul{
           margin:0;
           padding:0;
           li{
                @include listinline;
                padding:0 12px;
            
            i{
                cursor: pointer;
            }
           }
           
       } 

    }
    .chevron-up{
        @include chevronup;
        right:10px;
        bottom:30px; 
    }  
}
</style>