<template>
  <Section class="py-5">

    <!-- Content Top -->
    <div class="gb-container top text-center">
      <p class="text-capitalize fs-4">our core values</p>
      <div class="false-hr"></div>
      <p class="p-small lh-lg">Lorem ipsum dolor sit amet consectetur adipisicing elit. Quo nihil hic facilis. Quod repudiandae assumenda aliquid molestias recusandae odio dolorem incidunt, velit distinctio obcaecati eum.</p>
    </div>
    <!-- /Content Top -->



    <!-- Content Bottom -->
    <div class="bottom gb-container-big text-center py-5">
    
      <div class="container">
        <div class="row row-cols-4">
        
          <div v-for="(cardItem, index) in cards" :key="`cardItem-${index}`" 
           class="col">
            <div class="gb-card p-2">
              <div :style="{backgroundColor: `${cardItem.icon.color}`}" class="icon d-flex justify-content-center align-items-center p-1">
                <i :class="cardItem.icon.i"></i>
              </div>
              <span class="lh-lg">{{cardItem.title}}</span>
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
    transition: 1s;
    &:hover .icon{
      background-color: $primary-color !important;
    }
    &:hover span{
      color: $primary-color;
    }
    .icon{
      width: 90px;
      height: 90px;
      border-radius: 50%;
      margin: 5px auto;
      color: white;

      i{
        font-size: 2.8rem;
      }
    }

    span{
      color: $text-grey;
      font-size: .8rem;
    }
  }
}
</style>