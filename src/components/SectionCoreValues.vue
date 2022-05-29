<template>
  <Section class="py-5">

    <!-- Content Top -->
    <div class="gb-container top text-center">
      <p class="text-capitalize fs-4">our core values</p>
      <div class="false-hr"></div>
      <p class="p-small lh-lg mt-4">Lorem ipsum dolor sit amet consectetur adipisicing elit. Quo nihil hic facilis. Quod repudiandae assumenda aliquid molestias recusandae odio dolorem incidunt, velit distinctio obcaecati eum.</p>
    </div>
    <!-- /Content Top -->



    <!-- Content Bottom -->
    <div class="bottom gb-container-big text-center py-5">
    
      <div class="container">
        <div class="row row-cols-4">
        
          <div v-for="(cardItem, index) in cards" :key="`cardItem-${index}`" 
           class="col">
            <div class="gb-card">
              <div class="icon d-flex justify-content-center align-items-center p-1"><i :class="cardItem.icon"></i></div>
              <span class="fs-6">{{cardItem.title}}</span>
              <div :class="cardItem.hr"></div>
              <p class="p-small lh-lg">{{cardItem.text}}</p>
            </div>
          </div>

        </div>
      </div>

    </div>
    <!-- /Content Bottom -->
    
  </Section>
</template>

<script>
import cards from '../assets/data/section-core-values-col'

export default {
  name: 'SectionCoreValues',

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
  background-color: $tertiary-color;

  .gb-card{
    .icon{
      width: 90px;
      height: 90px;
      border: 1px solid $text-grey;
      border-radius: 50%;
      margin: 0 auto;
      color: blue;
    }

    span{
      color: $text-grey;
    }
  }
}
</style>