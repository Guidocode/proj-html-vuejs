<template>
  <Section> 

    <!-- Content Top -->
    <div class="top text-center">
      <p class="text-capitalize fs-4 pt-4">do you have a construction project we can help with?</p>
      <button type="button" class="btn btn-dark gb-btn">get a free quote</button>
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

            <div class="flip-card">
              <div class="flip-card-inner">
                <div class="flip-card-front p-3">
                  <div class="icon d-flex justify-content-center align-items-center p-1"><i :class="cardItem.icon"></i></div>
                  <span class="fs-4">{{cardItem.title}}</span>
                  <p class="p-small lh-lg">{{cardItem.text}}</p>
                </div>
                <div class="flip-card-back p-3">
                  <span class="fs-5 text-uppercase">Artfully Crafted</span>
                  <p class="p-small lh-lg">Lorem ipsum dolor sit amet consectetur adipisicing elit. Et sit magnam illo perferendis cum magni nisi esse, rerum reiciendis. Et!</p>
                  <button type="button" class="btn btn-dark gb-btn">get a quote</button>
                </div>
              </div>
            </div> 

            <!-- CARD FRONT -->
            <!-- <div class="gb-card p-3">
              <div class="icon d-flex justify-content-center align-items-center p-1"><i :class="cardItem.icon"></i></div>
              <span class="fs-4">{{cardItem.title}}</span>
              <p class="p-small lh-lg">{{cardItem.text}}</p>
            </div> -->

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
    /* Da sistemare (problema con le altezze) */
    .container{
      height: 200px;
    }

  

    // Flip card
    .flip-card {
      background-color: transparent;
      perspective: 1000px;
    }

    .flip-card-inner {
      position: relative;
      transition: transform 0.6s;
      transform-style: preserve-3d;
      box-shadow: 0 4px 8px 0 rgba(0,0,0,0.2);
    }

    .flip-card:hover .flip-card-inner {
      transform: rotateY(180deg);
    }

    .flip-card-front, .flip-card-back {
      position: absolute;
      -webkit-backface-visibility: hidden;
      backface-visibility: hidden;
      border-radius: 10px;
    }

    .flip-card-front{
      background-color: $tertiary-color;
      
      .icon{
        width: 50px;
        height: 50px;
        border: 1px solid $text-grey;
        border-radius: 50%;
        margin: 0 auto;
        color: $text-grey;
      }
    }

    .flip-card-back{
      background-color: $primary-color;
      transform: rotateY(180deg);

      .gb-btn{
        font-size: .8rem;
        @include primaryButton();
        border: 1px solid white;
        background-color: lighten($primary-color, 30%);
      }
    }
    // /Flip card

    // Front
    // .gb-card{
    //   background-color: $tertiary-color;
    //   border-radius: 10px;

    //   .icon{
    //     width: 50px;
    //     height: 50px;
    //     border: 1px solid $text-grey;
    //     border-radius: 50%;
    //     margin: 0 auto;
    //     color: $text-grey;
    //   }
    // }

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