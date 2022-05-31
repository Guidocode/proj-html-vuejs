<template>
  
  <div class="col">
    <div class="gb-card">
      <div class="front">
        <img class="img-fluid" :src="require(`../../assets/images/${card.image}`)" :alt="card.alt">
      </div>

      <div class="back d-flex justify-content-center align-items-center">
        <div class="content">
          <div class="buttons py-2">
            <div><a href="#"><i :class="card.link"></i></a></div>
            <div><a href="#"><i :class="card.search"></i></a></div>
          </div>
          <p>{{card.title}}</p>
          <span>{{card.subtitle}}</span>
        </div>
      </div>
      
    </div>
  </div>

</template>

<script>
export default {
  name: 'RecentWorkCard',

  props:{
    card: Object
  }
}
</script>

<style lang="scss" scoped>
@import '../../assets/style/vars';
@import '../../assets/style/mixins';

.gb-card{
  position: relative;
  .back{
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 308.5px;
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