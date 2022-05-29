<template>
  <Section class="h500 d-flex align-items-center">

    <div class="gb-container">
      <div class="container">
        <div class="row row-cols-4">

          <div v-for="(cardItem, index) in cards" :key="`cardItem-${index}`" 
           class="col">
            <div class="gb-card text-center">
              <i :class="cardItem.icon"></i>
              <div class="number">{{cardItem.number}}</div>
              <p class="title text-light fw-light">{{cardItem.title}}</p>
            </div>
          </div>

        </div>
      </div>
    </div>

  </Section>
</template>

<script>
import cards from '../assets/data/section-references'

export default {
  name: 'SectionReferences',

  data(){
    return{
      cards
    }
  }
}
</script>

<style lang="scss" scoped>
@import '../assets/style/vars';

section{
  background-image: url('../assets/images/home-244125289.jpg');
  background-size: cover;

  i, 
  .number{
    color: $primary-color;
    font-size: 50px;
  }

  .title{
    font-size: .7rem;
  }
}
</style>