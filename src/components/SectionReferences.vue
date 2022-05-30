<template>
  <Section class="h500 d-flex align-items-center">

    <div class="gb-container-big">
      <div class="container">
        <div class="row row-cols-4">

          <ReferencesCard 
          v-for="(cardItem, index) in cards" :key="`cardItem-${index}`" 
          :card="cardItem"
          />

        </div>
      </div>
    </div>

  </Section>
</template>

<script>
import cards from '../assets/data/section-references'
import ReferencesCard from './section-cards-comps/ReferencesCard.vue'

export default {
    name: "SectionReferences",
    data() {
      return {
        cards
      };
    },
    components: { ReferencesCard }
}
</script>

<style lang="scss" scoped>
section{
  background-image: url('../assets/images/home-244125289.jpg');
  background-size: cover;
}
</style>