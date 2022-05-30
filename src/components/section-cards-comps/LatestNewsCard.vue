<template>
  
  <div class="col">

    <div class="card">
      <img :src="require(`../../assets/images/${card.image}`)" class="card-img-top" :alt="card.alt">
      <div class="card-body text-start">
        <p class="fs-5">{{card.title}}</p>
        <span class="date">{{card.date}}</span>
        <div :class="card.hr"></div>
        <p class="p-small lh-lg">{{card.text}}</p>
      </div>
    </div>
    
  </div>

</template>

<script>
export default {
  name: 'LatestNewsCard',

  props:{
    card: Object
  }
}
</script>

<style lang="scss" scoped>
@import '../../assets/style/vars';
@import '../../assets/style/mixins';

.card{
  .date{
    font-size: .6rem;
    color: $text-grey;
  }
}
</style>