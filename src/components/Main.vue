<template>
  <main>
      <section id="portfolio-grid">
          <div class="col-lg-4">
              <img src="../assets/img/h-2-port-img-1.jpg" alt="">
          </div>
          <div class="col-lg-4">
              <img src="../assets/img/h-2-port-img-2.jpg" alt="">
          </div>
          <div class="col-lg-4">
              <img src="../assets/img/h-2-port-img-3.jpg" alt="">
          </div>
          <div class="col-lg-4 book" >
              <img src="../assets/img/h-2-port-img-4.jpg" alt="">
              <div class="text">
                  <h4>Illustration of novels</h4>
                  <h5>Illustration</h5>
              </div>
          </div>
          <div class="col-lg-4">
              <img src="../assets/img/h-2-port-img-5.jpg" alt="">
          </div>
          <div class="col-lg-4">
              <img src="../assets/img/h-2-port-img-6.jpg" alt="">
          </div>
      </section>
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
          
      </section>
      <section id="contactus">
        <h3>Want to work with us? Send us <span class="coursive">a message!</span></h3>
        <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Facilis, eius rem cumque impedit soluta commodi reprehenderit dolor ullam minima esse quaerat ratione error consequuntur odio expedita nisi porro cum enim.</p>  
        <button>Contact </button>
      </section>
      <section id="blog">
         <div class="col-lg-4">
             <div class="article">
              <div class="date">
                  <div class="decoration">07</div>
              </div>
              <img src="../assets/img/h-2-blog-img-1.jpg" alt=""> 
              <p>This way, loves: a detailed guide through new design</p>
              <h5>By Emily Fields</h5>  
             </div> 
         </div>
         <div class="col-lg-4">
             <div class="article">
                <div class="date">
                  <div class="decoration">07</div>
              </div> 
               <img src="../assets/img/h-2-blog-img-2.jpg" alt=""> 
               <p>I try to give people a different way of looking art</p> 
               <h5>By Emily Fields</h5>
             </div>   
         </div>
         <div class="col-lg-4">
             <div class="article">
                <div class="date">
                  <div class="decoration">07</div>
              </div>
                <img src="../assets/img/h-2-blog-img-3.jpg" alt="">
                <p>Introduce Richard Leperrière of those amazing features</p>
                <h5>By Emily Fields</h5>
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
#portfolio-grid{
    display: flex;
    flex-wrap: wrap;
    padding:40px 0;
    div{ 
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
#process{
    text-align: center;
    padding:50px 0px;
    background-image: url('../assets/svg/svg-3.svg') ;
    background-position: 50% 50%;
    background-repeat: no-repeat;
    h3{
        font-size:60px;
        .coursive{
              font-family: 'Courgette', cursive;
              font-weight: 600;
          }
    }
    .items-center{
        width:66%;
        margin: 50px auto;
        display:flex;
        justify-content: center;
        align-items: center;
        .item-description{
            display:flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            margin-top:20px;
            .circle-icon{
            display:flex;
            justify-content: center;
            align-items: center;
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
}
#contactus{
    display:flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    text-align: center;
    height:500px;
    background-size: cover;
    background-repeat: no-repeat;
    background-image:url("../assets/img/h-2-background-1.jpg");
    position:relative;
    h3{    
        margin-top:90px;
        font-size:65px;
        .coursive{
            font-family: 'Courgette', cursive;
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
          margin:30px 0px;
          font-family: 'Open Sans', sans-serif;
          text-transform: uppercase;
          font-size:14px;
          border:none;
          letter-spacing: 2px;
          font-weight:700;
          background-color:#D8F0E3;
          padding:20px 80px;
          &:hover{
              background-color:#E1C0B0;
              color: white;
          }
      }
      
}
#blog{
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
            .decoration{
            display:flex;
            justify-content: center;
            align-items: center;
            width:60px;
            height:40px;
            background-color:#C0E1CF;
            font-size: 28px;
            font-weight: 700;
            font-family: 'Courgette', cursive; 
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
            font-family: 'Courgette', cursive;
            
        }
    } 
        
        
}
</style>