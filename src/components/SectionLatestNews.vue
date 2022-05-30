<template>
  <Section class="py-5">


    <!-- Content Top -->
    <div class="top gb-container text-center">
      <span class="text-capitalize fs-4">Latest News</span>
      <div class="false-hr"></div>
      <p class="p-small lh-lg">Lorem ipsum dolor sit amet consectetur adipisicing elit. Sit laboriosam dignissimos, provident laborum, dolores corporis consequuntur nihil, eius repudiandae possimus molestias ex. Quidem, explicabo praesentium.</p>
    </div>
    <!-- /Content Top -->

    <!-- Content Bottom -->
    <div class="bottom gb-container-big text-center py-5">

      <!-- Cards -->
      <div class="container-fluid">
        <div class="row row-cols-3">

          <LatestNewsCard 
          v-for="(cardItem, index) in cards" :key="`cardItem-${index}`"
          :card="cardItem"
          />
          
        </div>
      </div>
      <!-- /Cards -->

      <!-- View All Projects -->
      <div class="container-fliud px-2 mt-5">
        <div class="row" row-cols-3>
          <div class="col d-flex align-items-center">
            <div class="false-hr-full"></div>
          </div>
          <div class="col">
            <button type="button" class="btn btn-dark gb-btn">view all projects</button>
          </div>
          <div class="col d-flex align-items-center">
            <div class="false-hr-full"></div>
          </div>
        </div>
      </div>
      <!-- /View All Projects -->

    </div>
    <!-- /Content Bottom -->

  </Section>
</template>

<script>
import LatestNewsCard from './section-cards-comps/LatestNewsCard.vue';
import cards from '../assets/data/section-latest-news-cards'
export default {
  name: "SectionLatestNews",

  data(){
    return{
      cards
    }
  },

  components: { LatestNewsCard }
}
</script>

<style lang="scss" scoped>
@import '../assets/style/vars';
@import '../assets/style/mixins';

section{
  background-color: $tertiary-color;

  .false-hr-full{
    background-color: white;
  }

  .gb-btn{
    background-color: $tertiary-color !important;
    color: $text-grey !important;
    width: 100%;
    border: 1px solid $tertiary-color;
    font-size: .9rem;
    &:hover{
      background-color: $primary-color !important;
    }
    @include secondaryButton();
  }
}
</style>