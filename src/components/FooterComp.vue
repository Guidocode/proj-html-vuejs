<template>
  <footer>
    
    <!-- Footer top -->
    <div class="footer-top py-5">
      <div class="container">
        <div class="row row-cols-4">

          <!-- Columns -->
          <div class="col">
            <div class="logo mb-4">
              <img class="w-100" src="../assets/images/footer-logo.png" alt="Logo">
            </div>
            <p class="p-small lh-lg">We are specialists in the construction of unique and exclusive properties. Our work inspires. We pride ourselves on delivering outstanding quality and design for leading clients across the world.</p>
            <button type="button" class="btn btn-warning gb-btn-primary">learn more</button>
          </div>


          <div id="latest-tweet" class="col">
            <h6 class="text-uppercase d-inline-block mb-4">latest tweets</h6>
            <div class="d-flex">
              <div class="left">
                <img src="../assets/images/3a74ce3d0532b7773b174c45ca3bd05a_bigger.png" alt="logo">
              </div>
              <div class="right">

                <div class="right-top d-flex justify-content-between">
                  <span class="fw-bold text-capitalize">theme fusion</span>
                  <img src="../assets/images/image (1).svg" alt="Twitter">
                </div>

                <span class="text-capitalize">@theme_Fusion</span>
                <p class="lh-sm">The layout of your website & how it is viewed on various mobile devices is essential for a positive user experience. Watch this explainer video that covers the main <a href="#">#Avada</a> layout options <a href="#">https://bit.ly/3rNzrCR</a> <a href="#">#WebsiteBuilder</a> <a href="#">#WordPress</a> <a href="#">#websitedesign</a></p>
                <img class="img-fluid" src="../assets/images/En2TRxLW4AEiWUN.jpeg" alt="">
                <div class="right-bottom d-flex justify-content-between">

                  <div class="bottom-left">
                    <img src="../assets/images/image (2).svg" alt="Heart">
                    <img src="../assets/images/image (3).svg" alt="Forward">
                    <!-- <img src="../assets/images/image.svg" alt=""> -->
                  </div>
                  <div class="bottom-right">
                    <span>22h</span>
                  </div>

                </div>
              </div>
            </div>
          </div>


          <div id="contact-us" class="col">
            <h6 class="text-uppercase d-inline-block mb-4">contact us today</h6>

            <div class="d-flex">
              <div class="left">
                <i class="fa-solid fa-globe"></i>
              </div>
              <div class="right mx-3 pt-1">
                <p class="p-small">Corporate Location <br> 1600 Amphitheatre Parkway <br> London WC1 1BA</p>
              </div>
            </div>

            <div class="d-flex">
              <div class="left">
                <i class="fa-solid fa-house-chimney"></i>
              </div>
              <div class="right mx-3 pt-1">
                <p class="p-small">Residential Location <br> 9521 Broadsberry Avenue <br> Paddington RC7 9ZA</p>
              </div>
            </div>

            <div class="d-flex">
              <div class="left">
                <i class="fa-solid fa-phone"></i>
              </div>
              <div class="right mx-3 pt-1">
                <p class="p-small">1.800.458.556 / 1.800.532.2112</p>
              </div>
            </div>

            <div class="d-flex">
              <div class="left">
                <i class="fa-solid fa-at"></i>
              </div>
              <div class="right mx-3 pt-1">
                <p class="p-small">info@your-domain.com</p>
              </div>
            </div>

            <div class="d-flex">
              <div class="left">
                <i class="fa-solid fa-clock"></i>
              </div>
              <div class="right mx-3 pt-1">
                <p class="p-small">Monday – Friday: 9:00 AM – 6:00 PM</p>
              </div>
            </div>

            <div class="d-flex">
              <div class="left">
                <i class="fa-solid fa-clock"></i>
              </div>
              <div class="right mx-3 pt-1">
                <p class="p-small">Saturday – Sunday: 9:00 AM – 12:00 PM</p>
              </div>
            </div>
          </div>


          <div id="find-us" class="col">
            <h6 class="text-uppercase d-inline-block mb-4">find us</h6>
            <a href="#"><img class="img-fluid" src="../assets/images/map.png" alt="map"></a>
          </div>
          <!-- /Columns -->

        </div>
      </div>
    </div>
    <!-- /Footer top -->

    <!-- Footer bottom -->
    <div class="footer-bottom d-flex justify-content-between align-items-center px-5 py-4">

      <div class="copy ">
        <p class="p-small mb-0">©COPYRIGHT 2012 - 2022 | AVADA THEME BY <span>THEMEFUSION</span> | ALL RIGHTS RESERVED | POWERED BY <span>WORDPRESS</span></p>
      </div>

      <div class="social d-flex justify-content-between">
        <div><i class="fa-brands fa-facebook-f"></i></div>
        <div><i class="fa-brands fa-twitter"></i></div>
        <div><i class="fa-brands fa-youtube"></i></div>
        <div><i class="fa-brands fa-instagram"></i></div>
      </div>

      <div class="chevron-up d-flex justify-content-center align-items-center">
        <a href="#"><i class="fa-solid fa-chevron-up text-light"></i></a>
      </div>

    </div>
    <!-- /Footer bottom -->

  </footer>
</template>

<script>
export default {
  name: 'FooterComp'
}
</script>

<style lang="scss" scoped>
@import '../assets/style/vars';
@import '../assets/style/mixins';

footer{
  background-color: #1E1E1E;

  .logo{
    width: 150px;
  }

  .gb-btn-primary{
    @include primaryButton();
  }

  h6{
    color: $primary-color;
  }

  i{
    font-size: .8rem;
    color: $text-grey;
  }

  #latest-tweet{
    color: white;
    .left{
      img{
        border-radius: 50%;
        width: 30px;
        margin: 5px;
      }
    }

    .right{
      .right-top{
        margin-bottom: -12px;
        img{
          width: 15px;
        }
      }

      span{
        font-size: .7rem;
        margin-right: 10px;
      }
      p{
        font-size: .7rem;
      }
      img{
        border-radius: 5px;
      }

      .right-bottom{
        .bottom-left{
          img{
            width: 15px;
            margin-right: 10px;
          }
        }
        .bottom-right{
          span{
            color: $text-grey;
          }
        }
      }
    }
  }

  .footer-bottom{
    background-color: black;
    .copy{
      span{
        color: $tertiary-color;
      }
    }

    .social{
      width: 8%;
    }
  }

  .chevron-up{
    position: fixed;
    bottom: 0;
    right: 200px;
    width: 40px;
    height: 30px;
    background-color: #333232a8;
    border-radius: 3px;
  }
  
}
</style>