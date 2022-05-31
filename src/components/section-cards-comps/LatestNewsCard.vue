<template>
  
  <div class="col">

    <div class="card">

      <div class="front">
        <img :src="require(`../../assets/images/${card.image}`)" class="card-img-top" :alt="card.alt">
      </div>

      <div class="back d-flex justify-content-center align-items-center">
        <div class="content px-5">
          <div class="buttons py-2">
            <div><a href="#"><i :class="card.link"></i></a></div>
            <div><a href="#"><i :class="card.search"></i></a></div>
          </div>
          <p>{{card.backtitle}}</p>
          <span>{{card.subtitle}}</span>
        </div>
      </div>
      
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
  .front{
    position: relative;
  }

    .back{
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 184.8px;
    background-color: $primary-color;
    cursor: pointer;
    transition: all .3s;
    opacity: 0;
    &:hover{
      opacity: 1;
    }

    .buttons{
      display: flex;
      justify-content: space-evenly;
      div{
        display: flex;
        justify-content: center;
        align-items: center;
        background-color: #FFFAEA;
        width: 50px;
        height: 50px;
        padding: 5px;
        border-radius: 50%;

        i{
          color: $primary-color;
        }
      }
    }
    p, span{
      color: #FFFAEA;
      font-weight: normal;
    }
    span{
      font-size: .8rem;
    }
  }
}
</style>