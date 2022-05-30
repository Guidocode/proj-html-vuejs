<template>
  <Section class="d-flex align-items-center pb-5">

    <div class="container-fluid">
      <div class="row gb-container-big text-start py-5">

        <div class="left col-8 pt-5">
          <span class="text-capitalize fs-3 d-inline-block">Building inspiring spaces</span>
          <div class="false-hr"></div>
          <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Temporibus magnam ratione, sint magni libero itaque!</p>
        </div>

        <div class="right col-4 text-end pt-5">
          <div class="d-inline-block text-center">
            <button type="button" class="btn btn-warning gb-btn-primary">get a free quote</button> <br>
            <span class="text-capitalize fw-normal">Only takes a few seconds!</span>
          </div>
        </div>

      </div>
    </div>


  </Section>
</template>

<script>
export default {
  name: 'SectionBuildInspiring'
}
</script>

<style lang="scss" scoped>
@import '../assets/style/vars';
@import '../assets/style/mixins';

section{
  background-image: url('../assets/images/about-call-to-action-57862405.jpeg');
  background-size: cover;
  background-position-y: center;
  color: white;

  .container-fluid{
    background-image: url('../assets/images/about-call-to-action-57862405.jpeg');
    background-size: cover;
    background-position-y: 80%;

    .left{
      .false-hr{
        margin: 20px 0;
      }
    }
    
    .right{
      .gb-btn-primary{
        @include primaryButton();
      }

      span{
        font-size: .7rem;
      }
    }
    
  }
}
</style>