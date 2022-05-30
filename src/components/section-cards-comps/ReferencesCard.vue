<template>
  
  <div class="col">
    <div class="gb-card text-center">
      <i :class="card.icon"></i>
      <div class="number fw-normal">{{card.number}}</div>
      <p class="title text-light">{{card.title}}</p>
    </div>
  </div>

</template>

<script>
export default {
  name: 'ReferencesCard',

  props:{
    card: Object
  }
}
</script>

<style lang="scss" scoped>
@import '../../assets/style/vars';

i, .number{
  color: $primary-color;
  font-size: 50px;
}
.title{
  font-size: .8rem;
}
</style>