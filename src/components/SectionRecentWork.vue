<template>
  <Section class="py-5">

    <!-- Content Top -->
    <div class="top gb-container text-center">
      <p class="text-capitalize fs-4">Explore Recent Work</p>
      <div class="false-hr"></div>
      <p class="p-small lh-lg mt-4">Lorem ipsum dolor sit, amet consectetur adipisicing elit. Nulla quia maiores, corrupti velit accusamus, autem pariatur repudiandae mollitia ducimus ullam ipsam, in animi natus ratione.</p>
    </div>
    <!-- /Content Top -->



    <!-- Content Bottom -->
    <div class="bottom gb-container-big text-center py-3">

      <!-- Cards -->
      <div class="container-fluid">
        <div class="row row-cols-3">

          <div v-for="(imgItem, index) in images" :key="`imgItem-${index}`" 
           class="col">
            <div class="gb-card">
              <img class="img-fluid" :src="require(`../assets/images/${imgItem.image}`)" :alt="imgItem.alt">
            </div>
          </div>

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
import images from '../assets/data/section-recent-work-img'

export default {
  name: 'SectionRecentWork',

  data(){
    return{
      images
    }
  }
}
</script>

<style lang="scss" scoped>
@import '../assets/style/vars';
@import '../assets/style/mixins';

section{
  .gb-btn{
    background-color: white !important;
    color: $text-grey !important;
    width: 100%;
    border: 1px solid white;
    font-size: .9rem;
    &:hover{
      background-color: $primary-color !important;
    }
    @include secondaryButton();
  }
}
</style>