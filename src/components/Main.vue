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
                <p>Lorem ipsum, dolor sit amet consectetur adipisicing.</p> 
              </div>
              <div class="item-description">
                <div class="circle-icon">
                    <i style="color:#F8D12D" class="far fa-comment"></i>
                </div>
                <h4>Than we talk about</h4>
                <p>Lorem ipsum, dolor sit amet consectetur adipisicing.</p> 
              </div>
              <div class="item-description">
                <div class="circle-icon">
                    <i style="color:#80465F" class="fas fa-cloud"></i>
                </div>
                <h4>And we think about</h4>
                <p>Lorem ipsum, dolor sit amet consectetur adipisicing.</p> 
              </div>
              <div class="item-description">
                <div class="circle-icon">
                  <i style="color:#EB6950" class="fas fa-marker"></i>
                </div> 
                <h4>So we draw along</h4> 
                <p>Lorem ipsum, dolor sit amet consectetur adipisicing.</p> 
              </div>
          </div>
          
      </section>
      <section></section>
      <section></section>
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
                font-weight: 300;
                color:#A6A6A6;
                letter-spacing: 1.2px;
                margin:10px 0;
                width:80%;
            }
        }
       
    }
}

</style>