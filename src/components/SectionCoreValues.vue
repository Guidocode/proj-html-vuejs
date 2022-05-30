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
        
          <!-- Cards -->
          <CoreValuesCard 
          v-for="(cardItem, index) in cards" :key="`cardItem-${index}`" 
          :card="cardItem"
          />
          <!-- /Cards -->

        </div>
      </div>

    </div>
    <!-- /Content Bottom -->
    
  </Section>
</template>

<script>
import cards from '../assets/data/section-core-values-col'
import CoreValuesCard from './section-cards-comps/CoreValuesCard.vue'

export default {
    name: "SectionCoreValues",
    data() {
        return {
            cards
        };
    },
    components: { CoreValuesCard }
}
</script>

<style lang="scss" scoped>
@import '../assets/style/vars';
@import '../assets/style/mixins';

section{
  background-color: $tertiary-color;
}
</style>