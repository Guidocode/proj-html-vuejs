<template>
  
  <div class="col">
    <div class="gb-card p-2">
      <div :style="{backgroundColor: `${card.icon.color}`}" class="icon d-flex justify-content-center align-items-center p-1">
        <i :class="card.icon.i"></i>
      </div>
      <span class="lh-lg">{{card.title}}</span>
      <div :class="card.hr"></div>
      <p class="p-small lh-lg">{{card.text}}</p>
    </div>
  </div>

</template>

<script>
export default {
  name: 'CoreValuesCard',

  props:{
    card: Object
  }

}
</script>

<style lang="scss" scoped>
@import '../../assets/style/vars';
@import '../../assets/style/mixins';

.gb-card{
  transition: 1s;
  &:hover .icon{
    background-color: $primary-color !important;
    animation: pulse 1.5s infinite;
    animation-timing-function: ease-in-out;  

    @keyframes pulse {
      0% { transform: scale(1) };
      50% { transform: scale(1.2)};
      100% { transform: scale(1); }
    }
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
</style>


.pulse a:hover{ 
   
}

