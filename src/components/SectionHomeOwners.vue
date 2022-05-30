<template>
  <Section class="d-flex justify-content-center align-items-center h500">

    <!-- Content -->
    <div class="content gb-container text-center">
      <span class="text-capitalize fs-4">Our Home Owners Say</span>
      <div class="false-hr"></div>
      <div class="user-image img-fluid"></div>
      <p class="fst-italic fw-normal">"No man but feels more of a man in the world if he have but a bit of ground <br> that he can call his own. However small it is on the surface, it is four thousand <br> miles deep; and that is a very handsome property.”</p>
      <span class="client text-uppercase fw-bold">HARRY SMITH • NEW HOME OWNER</span>
      <div class="fake-button">
        <div class="prev active"></div>
        <div class="next"></div>
      </div>
    </div>
    <!-- /Content -->

  </Section>
</template>

<script>
export default {
  name: 'SectionHomeOwners'
}
</script>

<style lang="scss" scoped>
section{
  background-image: url('../assets/images/home-parallax-144609983.jpg');
  background-size: cover;
  background-position-y: center;
  color: white;
  .user-image{
    width: 120px;
    height: 120px;
    background-image: url('../assets/images/home-testimonial-113165296.jpg');
    background-size: cover;
    margin: 10px auto;
    border-radius: 50%;
  }

  p{
    font-size: .9rem;
  }

  .fake-button{
    margin: 20px auto;
    .prev,
    .next{
      display: inline-block;
      width: 10px;
      height: 10px;
      background-color: transparent;
      border: 1px solid white;
      border-radius: 50%;
      margin: 0 5px;
    }

    .active{
      background-color: white;
    }
  }
  

}
</style>