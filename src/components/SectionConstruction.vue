<template>
  <Section> 

    <!-- Content Top -->
    <div class="top text-center">
      <p class="text-capitalize fs-4 pt-4">do you have a construction project we can help with?</p>
      <button type="button" class="btn btn-dark gb-btn-secondary">get a free quote</button>
    </div>
    <!-- /Content Top -->



    <!-- Content Bottom -->
    <div class="bottom text-center py-5">

      <div class="gb-container text-center">
        <p class="text-capitalize fs-4">specialists in modern construction</p>
        <div class="false-hr"></div>
        <p class="p-small lh-lg mt-4 mb-5">Lorem ipsum dolor sit amet consectetur adipisicing elit. Dolorum sed sequi, dolor, nostrum aliquam illo repellendus enim ea at commodi, veniam doloribus omnis molestias!</p>
      </div>

      <div class="container">
        <div class="row row-cols-4">

          <div v-for="(cardItem, index) in cards" :key="`cardItem-${index}`" 
           class="col">

            <!-- <div class="flip-card">
              <div class="flip-card-inner">
                <div class="flip-card-front">
                  <img src="img_avatar.png" alt="Avatar" style="width:300px;height:300px;">
                </div>
                <div class="flip-card-back">
                  <h1>John Doe</h1>
                  <p>Architect & Engineer</p>
                  <p>We love that guy</p>
                </div>
              </div>
            </div>  -->

            <!-- CARD FRONT -->
            <div class="gb-card p-3">
              <div class="icon d-flex justify-content-center align-items-center p-1"><i :class="cardItem.icon"></i></div>
              <span class="fs-4">{{cardItem.title}}</span>
              <p class="p-small lh-lg">{{cardItem.text}}</p>
            </div>

            <!-- CARD BACK -->
            <!-- <div class="gb-card p-3">
              <span class="fs-5 text-uppercase">Artfully Crafted</span>
              <p class="p-small lh-lg">Lorem ipsum dolor sit amet consectetur adipisicing elit. Et sit magnam illo perferendis cum magni nisi esse, rerum reiciendis. Et!</p>
              <button type="button" class="btn btn-dark gb-btn">get a quote</button>
            </div> -->

          </div>

        </div>
      </div>

    </div>
    <!-- /Content Bottom -->

  </Section>
</template>

<script>
import cards from '../assets/data/section-construction-cards'

export default {
  name: 'SectionConstruction',

  data(){
    return{
      cards
    }
  }
}
</script>

<style lang="scss" scoped>
@import '../assets/style/vars';
@import '../assets/style/mixins';

section{
  font-weight: 200;
  color: $secondary-color;
  
  .top{
    background-color: $primary-color;
    height: 90px;
    margin-bottom: 30px;

    .gb-btn{
      font-size: .8rem;
      @include secondaryButton();
      border: 1px solid white;
      &:hover{
        background-color: white;
        color: $secondary-color;
        border: 1px solid $secondary-color;
      }
    }
  }

  .bottom{
    .false-hr{
      max-width: 30%;
      height: 1px;
      background-color: $primary-color;
      margin: 0 auto;
    }

    .p-small{
      font-size: .7rem;
      color: $text-grey;;
    }

    // Front
    .gb-card{
      background-color: $tertiary-color;
      border-radius: 10px;

      .icon{
        width: 50px;
        height: 50px;
        border: 1px solid $text-grey;
        border-radius: 50%;
        margin: 0 auto;
        color: $text-grey;
      }
    }

    // Back
    // .gb-card{
    //   background-color: $primary-color;

    //   .gb-btn{
    //     font-size: .8rem;
    //     @include primaryButton();
    //     border: 1px solid white;
    //     background-color: lighten($primary-color, 30%);
    //   }
    // }

    
  }

  
}

</style>