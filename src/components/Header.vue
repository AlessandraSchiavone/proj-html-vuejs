<template>
  <header>
      <!-- section dedicata alla nav-bar e al logo  -->
      <section id="nav-bar">
          <img src="../assets/img/logo-sidearea-1.png" alt="Logo Maree">
          <ul class="list-inline">
              <li v-for="(item,index) in items" :key="index">
                    <a :href="item.url">
                        <span @click="toggleActive(index)" :class="{active: item.active}">
                            {{ item.name }}
                        </span>
                    </a>
              </li>
              <li>
                  <a href="">
                      <img src="../assets/svg/svg-1.svg" alt="All">
                  </a>      
             </li>
          </ul>
      </section>
      <!-- section jumbotron -->
      <section id="jumbotron">
          <!-- chevron laterale dello slider -->
          <div class="chevron">
              <span class="circle">
                  <i class="fas fa-chevron-left"></i>
              </span>
          </div> 
          <!-- box contenitore della parte centrale suddiviso in due colonne della stessa dimensione e dallo slier-items    -->
          <div class="box">
                <!-- colonna di sinistra -->
                <div class="colsx col-lg-6">
                    <!-- titolo e bottone -->
                    <div class="col-lg-8 offset-lg-4">
                        <h1>Devotion that never <span class="coursive">ends</span></h1>
                        <h4>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Similique, molestias!</h4>
                        <button id="bt-white"> Read More </button>
                    </div>
                </div>
                <!-- colonna di destra suddivisa in riga e sottorighe per ottenere l'immagine finale -->
                <div class="coldx col-lg-6">
                    <div class="row-1">
                        <img src="../assets/img/short-slider-rev-1-img-2.png">
                        <img src="../assets/img/h-2-slider-img-14.png">
                    </div>
                    <div class="row-2">
                        <div class="subrow-1">
                            <img src="../assets/img/h-2-slider-img-12.png"> 
                        </div>
                        <div class="subrow-2">
                            <img src="../assets/img/h-2-slider-img-13.png">  
                        </div>
                            <img src="../assets/img/h-2-slider-img-15.png">
                            <img src="../assets/img/h-2-slider-img-16.png">
                        <div class="subrow-3">
                                <img src="../assets/img/short-slider-rev-1-img-6.png">
                        </div>
                        <div class="subrow-4">
                            <img src="../assets/img/h-2-slider-img-17.png" > 
                        </div>
                    </div>
                </div>   
                <div class="slider-items">
                    <span class="small-circle"></span>
                    <span class="small-circle"></span>
                    <span class="small-circle"></span>
                </div>
          </div>
        <!-- chevron laterale dello slider -->
          <div class="chevron">
              <span class="circle">
                  <i class="fas fa-chevron-right"></i>
              </span>
          </div>     
      </section>
  </header>
</template>

<script>
export default {
    name:"Header",
    props:["items"],
    methods: {
        toggleActive: function(index) {
            this.items[index].active = !this.items[index].active;
            for(let i=0; i< this.items.length;i++){
                if(i!=index){
                    this.items[i].active = false;
                } 
            }
            return(this.items[index].active)
        }
    }
}
</script>

<style lang="scss" scoped>
@import '../style/mixin';
@import "../style/variables";
#nav-bar{
    font-family: $fontOpen;
    @include spacebetween;
    align-items:center;
    padding:40px 30px;
    height: 80px;
    img{
        padding:5px;
    }
    .list-inline{
        padding:0;
        margin:0;
        li{ 
            @include listinline;
            padding:0px 20px;
            line-height:19px;
            letter-spacing: 3px;  
            text-transform: uppercase;
            font-weight: 700;
            font-size: 14px;
            a{
                text-decoration: none;
                color:black;
                span{
                    cursor:pointer;
                    display: inline-block;
                &.active {
                    line-height: 6px;  
                    border-bottom:5px solid #F5D8CA;
                    }
                }
            }
            img{
                vertical-align: middle;
            }
        }
    }
}
#jumbotron{
    @include spacebetween;
    height:600px;
    padding:0px 20px;
    .chevron{
        @include center;
        height:100%;
       .circle{
           @include center;
            height:30px;
            width:30px;
            color:white;
            border-radius:50%;
            cursor: pointer;
            background-color:#E1C0B0 ;
            padding:5px;
        }   
    }
    .box{
        @include wrap;
    .colsx{
      height:100%;
      padding:50px 10px; 
      h1{
          padding-top:30px;
          font-size:85px;
          font-weight:300;
          .coursive{
            font-family: $Corsive;
            font-weight: 600;
          }
        }
      h4{
          width:85%;
          padding:5px 0px;
          color:#878787;
          font-weight: 100;
          font-size: 22px;
          line-height: 1.4;
          letter-spacing: 1.2px;
      }
      button{
          @include button;
          border:3px solid #E1C0B0;
          background-color: white;
          padding:18px 45px;
      } 
    }
    .coldx{
        height:100%;
        padding:50px 0px;
        .row-1{
            width:660px;
            @include spacebetween;
        }
        .row-2{
            display: flex;
            position:relative;
            .subrow-1{
                position:absolute;
                left:-80px;
                bottom:180px;
            }
            .subrow-2{
                position:absolute;
                bottom:4px;
                left:-10px;
            }
            .subrow-3{
                @include flexend;
                position:absolute;
                top:50px;
                width:700px;    
            }
            .subrow-4{
                @include flexend;
                position:absolute;
                bottom:0px;  
                width:800px;     
            }
        }    
    }
    .slider-items{
        width:100%;
        @include center;
        .small-circle{
            height:10px;
            width:10px;
            border-radius:50%;
            margin:0 15px;
            cursor: pointer;
            background-color:#E1C0B0 ;
        }
    }
    }   
}
</style>