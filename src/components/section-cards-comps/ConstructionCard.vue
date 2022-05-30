<template>
  
  <div class="col">
    <div class="flip-card">
      <div class="flip-card-inner">
        <div class="flip-card-front p-3">
          <div class="icon d-flex justify-content-center align-items-center p-1"><i :class="card.icon"></i></div>
          <span class="fs-4">{{card.title}}</span>
          <p class="p-small lh-lg">{{card.text}}</p>
        </div>
        <div class="flip-card-back p-3">
          <span class="fs-5 text-uppercase">Artfully Crafted</span>
          <p class="p-small lh-lg">Lorem ipsum dolor sit amet consectetur adipisicing elit. Et sit magnam illo perferendis cum magni nisi esse, rerum reiciendis. Et!</p>
          <button type="button" class="btn btn-dark gb-btn">get a quote</button>
        </div>
      </div>
    </div>
  </div>

  <!-- CARD FRONT -->
  <!-- <div class="gb-card p-3">
    <div class="icon d-flex justify-content-center align-items-center p-1"><i :class="card.icon"></i></div>
    <span class="fs-4">{{card.title}}</span>
    <p class="p-small lh-lg">{{card.text}}</p>
  </div> -->

  <!-- CARD BACK -->
  <!-- <div class="gb-card p-3">
    <span class="fs-5 text-uppercase">Artfully Crafted</span>
    <p class="p-small lh-lg">Lorem ipsum dolor sit amet consectetur adipisicing elit. Et sit magnam illo perferendis cum magni nisi esse, rerum reiciendis. Et!</p>
    <button type="button" class="btn btn-dark gb-btn">get a quote</button>
  </div> -->

</template>

<script>
export default {
  name: 'ConstructionCard',

  props:{
    card: Object
  }
}
</script>

<style lang="scss" scoped>
@import '../../assets/style/vars';
@import '../../assets/style/mixins';

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
  height: 100%;
}
.flip-card:hover .flip-card-inner {
  transform: rotateY(180deg);
}
.flip-card-front, .flip-card-back {
  position: absolute;
  -webkit-backface-visibility: hidden;
  backface-visibility: hidden;
  border-radius: 10px;
  min-height: 202px;
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
</style>