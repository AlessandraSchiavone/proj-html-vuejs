<template>
  <main>
      <!-- suddivisione del main in 4 section -->
      <!-- sezione portfolio  -->
      <section id="portfolio">
          <div class="grid-row">
                <div class="col-lg-4">
                    <img src="../assets/img/h-2-port-img-1.jpg">
                </div>
                <div class="col-lg-4">
                    <img src="../assets/img/h-2-port-img-2.jpg">
                </div>
                <div class="col-lg-4">
                    <img src="../assets/img/h-2-port-img-3.jpg">
                </div>
                <div class="chevron-up">
                    <a href="/">
                        <img src="../assets/svg/svg-2.svg" alt="Up">
                    </a>    
                </div> 
           </div>
           <div class="grid-row">
                <div class="chevron-up">
                    <a href="/">
                        <img src="../assets/svg/svg-2.svg" alt="Up">
                    </a>    
                </div>
                <div class="col-lg-4 book" >
                    <img src="../assets/img/h-2-port-img-4.jpg" alt="Book">
                    <!-- effetto hover -->
                    <div class="text">
                        <h4>Illustration of novels</h4>
                        <h5>Illustration</h5>
                    </div>
                </div>
                <div class="col-lg-4">
                    <img src="../assets/img/h-2-port-img-5.jpg" >
                </div>
                <div class="col-lg-4">
                    <img src="../assets/img/h-2-port-img-6.jpg" >
                </div>  
            </div>  
      </section>
      <!-- sezione process -->
      <section id="process">
            <h3>Working <span class="coursive">process</span></h3>
            <div class="items-center">
                <div class="item-description">
                    <div class="circle-icon">
                        <i style="color:#BADAC9" class="fas fa-lightbulb"></i>
                    </div> 
                    <h4>First theres an idea</h4>
                    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Culpa, tempora?</p> 
                </div>
                <div class="item-description">
                    <div class="circle-icon">
                        <i style="color:#F8D12D" class="far fa-comment"></i>
                    </div>
                    <h4>Than we talk about</h4>
                    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Culpa, tempora?</p> 
                </div>
                <div class="item-description">
                    <div class="circle-icon">
                        <i style="color:#80465F" class="fas fa-cloud"></i>
                    </div>
                    <h4>And we think about</h4>
                    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Culpa, tempora?</p> 
                </div>
                <div class="item-description">
                    <div class="circle-icon">
                    <i style="color:#EB6950" class="fas fa-marker"></i>
                    </div> 
                    <h4>So we draw along</h4> 
                    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Culpa, tempora?</p> 
                </div>   
            </div>
            <div class="chevron-up">
                <a href="/">
                    <img src="../assets/svg/svg-2.svg" alt="Up">
                </a>    
            </div>  
      </section>
      <!-- sezione contatti -->
      <section id="contactus">
            <h3>Want to work with us? Send us <span class="coursive">a message!</span></h3>
            <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Facilis, eius rem cumque impedit soluta commodi reprehenderit dolor ullam minima esse quaerat ratione error consequuntur odio expedita nisi porro cum enim.</p>  
            <button>Contact </button>
      </section>
      <!-- sezione blog -->
      <section id="blog">
        <div class="chevron-up">
          <a href="/">
              <img src="../assets/svg/svg-2.svg" alt="Up">
          </a>    
        </div>
        <div class="box-blog">
            <div class="col-lg-4">
                <div class="article">
                <!-- decorazione linguetta per la data -->
                    <div class="date">
                        <div class="decoration-1">07</div>
                        <div class="decoration-2">May' 19</div>
                        <div class="ribbon">
                            <div class="decoration-3"></div>
                            <div class="decoration-4"></div>
                        </div>  
                    </div>
                    <img src="../assets/img/h-2-blog-img-1.jpg" > 
                    <p>This way, loves: a detailed guide through new design</p>
                    <h5>By Emily Fields</h5>  
                </div> 
            </div>
            <div class="col-lg-4">
                <div class="article">
                <!-- decorazione linguetta per la data -->
                    <div class="date">
                        <div class="decoration-1">07</div>
                        <div class="decoration-2">May' 19</div>
                        <div class="ribbon">
                            <div class="decoration-3"></div>
                            <div class="decoration-4"></div>
                        </div>
                    </div> 
                    <img src="../assets/img/h-2-blog-img-2.jpg" > 
                    <p>I try to give people a different way of looking art</p> 
                    <h5>By Emily Fields</h5>
                </div>   
            </div>
            <div class="col-lg-4">
                <div class="article">
                <!-- decorazione linguetta per la data -->     
                    <div class="date">
                        <div class="decoration-1">07</div>
                        <div class="decoration-2">May' 19</div>
                        <div class="ribbon">
                            <div class="decoration-3"></div>
                            <div class="decoration-4"></div>
                        </div>
                    </div>
                    <img src="../assets/img/h-2-blog-img-3.jpg" >
                    <p>Introduce Richard Leperrière of those amazing features</p>
                    <h5>By Emily Fields</h5>
                </div>     
            </div>   
        </div>        
      </section>
  </main>
</template>

<script>
export default {
    name:"Main"
}
</script>

<style lang="scss" scoped>
@import '../style/mixin';
@import "../style/variables";
#portfolio{
    padding:40px 0;
    .grid-row{
        position:relative;
        @include wrap; 
        .chevron-up{ 
            @include chevronup;
            right:10px;
            bottom:30px;
        }  
        .col-lg-4{ 
            position:relative;
            img{
                width:100%;
            }
            &.book{
                cursor: pointer;
                .text{ 
                        display: none;
                        position:absolute;
                        bottom:250px;
                        width:50%;
                        background-color:white;
                        padding:18px;
                        h5{
                            font-style: italic;
                            font-size:18px ;
                            }
                    }   
                }
            &.book:hover .text{
                display:block;
            }  
        }        
    }
}
#process{
    text-align: center;
    padding:50px 0px;
    background-image: url('../assets/svg/svg-3.svg') ;
    background-position: 50% 50%;
    background-repeat: no-repeat;
    position:relative;
    h3{
        font-size:60px;
        .coursive{
            font-family: $Corsive;
            font-weight: 600;
        }
    }
    .items-center{
        width:66%;
        margin: 50px auto;
        @include center;
        .item-description{
            @include center;
            flex-direction: column;
            margin-top:20px;
            .circle-icon{
            @include center;
            width:160px;
            height:160px;
            border-radius: 50%;
            background-color: #FAF7F1;
                i{
                    font-size: 50px;
                }
            }
            h4{
                margin-top:20px;
            }
            p{  
                font-size:14px;
                font-weight: 300;
                color:#878787;
                letter-spacing: 1.2px;
                margin:10px 0;
            }
        }    
    }
    .chevron-up{
        @include chevronup;
        right:10px;
        bottom:30px;       
    }  
}
#contactus{
    display:flex;
    flex-direction: column;
    @include center;
    height:500px;
    background-size: cover;
    background-repeat: no-repeat;
    background-image:url("../assets/img/h-2-background-1.jpg");
    position:relative;
    h3{    
        margin-top:90px;
        font-size:65px;
        .coursive{
            font-family: $Corsive;
            font-weight: 600;
        }
    }
    p{
        font-size:20px;
        font-weight: 300;
        color:#878787;
        letter-spacing: 1.2px;
        margin:10px 0;
        width:70%;
    }
    button{
        @include button;
        border:none;
        background-color:#D8F0E3;
        padding:20px 80px;
    }      
}
#blog{
    position:relative; 
    .chevron-up{
        @include chevronup;
        right:10px;
        top:-60px;    
    }
    .box-blog{
        display:flex;
        width:70%;
        margin:120px auto;
        .article{
            margin-left:30px;
            position:relative;
            .date{
                position:absolute;
                padding:5px;
                left:20px;
                top:-20px;
                .decoration-1{
                    @include center;
                    width:60px;
                    height:40px;
                    background-color:#C0E1CF;
                    font-size: 28px;
                    font-weight: 700;
                    font-family:$Corsive; 
                }
                .decoration-2{
                    padding:2px;
                    background-color: #F3D0C7;
                    text-align: center;
                    text-transform: uppercase;
                    letter-spacing: 1.2px;
                    font-size:11px;
                    font-weight: 700;      
                }
                .ribbon{
                    display:flex;
                    .decoration-3{
                        @include ribbon;
                        border-right: 30px solid transparent;
                    }
                    .decoration-4{
                        @include ribbon;
                        border-left: 30px solid transparent;
                    }
                }        
            }
            img{
                width:100%;
            } 
            p{
                font-size: 26px;
                margin:25px 0px 15px 0px;
            }
            h5{
                font-size: 16px;
                font-family: $Corsive;   
            }
        } 
    }          
}
</style>