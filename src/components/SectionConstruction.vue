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
        <p class="p-small lh-lg mb-5">Lorem ipsum dolor sit amet consectetur adipisicing elit. Dolorum sed sequi, dolor, nostrum aliquam illo repellendus enim ea at commodi, veniam doloribus omnis molestias!</p>
      </div>

      <div class="container">
        <div class="row row-cols-4">

          <ConstructionCard 
          v-for="(cardItem, index) in cards" :key="`cardItem-${index}`"
          :card="cardItem"
          />

          <div  
           class="col">

          </div>

        </div>
      </div>

    </div>
    <!-- /Content Bottom -->

  </Section>
</template>

<script>
import cards from '../assets/data/section-construction-cards'
import ConstructionCard from './section-cards-comps/ConstructionCard.vue'

export default {
    name: "SectionConstruction",
    data() {
        return {
            cards
        };
    },
    components: { ConstructionCard }
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
      width: 85%;
    }
    
  }
  
}

</style>