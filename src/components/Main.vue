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
      <section></section>
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

</style>