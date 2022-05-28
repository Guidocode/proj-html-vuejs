<template>
  <div class="jumbo d-flex justify-content-center align-items-center h500">

    <!-- Box -->
    <div class="box">
      <div class="demos text-center p-1 mb-2">
        <i class="fa-solid fa-folder-closed"></i> <br>
        <span>Demos</span>
      </div>
      <div class="on-sale text-center p-1">
        <span class="price text-success fw-bold">$39</span> <br>
        <span>On-Sale</span>
      </div>
    </div>
    <!-- /Box -->

    <!-- Content Jumbo -->
    <div class="content-jumbo gb-container text-center">
      <h1 class="text-uppercase text-light fw-bold">building inspiring spaces</h1>
      <p>We Build Inspiring Residential & Commercial Spaces</p> 
      <button type="button" class="btn btn-dark gb-btn-secondary">explore recent work</button>
      <button type="button" class="btn btn-warning gb-btn-primary">get a quote today</button> 
    </div>
    <!-- /Content Jumbo -->

  </div>
</template>

<script>
export default {
  name: 'JumboComp'
}
</script>

<style lang="scss" scoped>
@import '../assets/style/vars';
@import '../assets/style/mixins';

.jumbo{
  position: relative;
  background-image: url('../assets/images/home-slider-62528242.jpg');
  background-size: cover;

  p{
    color: $primary-color;
    font-weight: 200;
    margin: 25px 0;
  }

  .gb-btn-secondary{
    @include secondaryButton();
    margin-right: 15px
  }

  .gb-btn-primary{
    @include primaryButton();
  }

  .box{
    position: absolute;
    top: 10px;
    right: 10px;

    .demos,
    .on-sale{
    font-size: .5rem;
    background-color: white;
    border-radius: 5px;
    color: black;
    cursor: pointer;
    }

    i, .price{
      font-size: 15px;
    }
  }
}
</style>