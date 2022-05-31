<template>
  <Section class="d-flex justify-content-center align-items-center h500">

    <!-- Content -->
    <div class="content gb-container text-center">
      <span class="text-capitalize fs-4">Our Home Owners Say</span>
      <div class="false-hr"></div>


      <!-- Testimonials -->
      <div class="testimonials">
        <img class="user-image img-fluid " :src="require(`../assets/images/${slides[indexCurrentSlide].image}`)" :alt="slides[indexCurrentSlide].alt">
        <p class="fst-italic fw-normal">{{slides[indexCurrentSlide].text}}</p>
        <span class="client text-uppercase fw-bold">{{slides[indexCurrentSlide].name}}</span>
      </div>
      <!-- /Testimonials -->

      <!-- Buttons -->
      <div>
        <div v-for="(slide, index) in slides" :key="`slide-${index}`"
        class="btn-current-slide" @click="currentSlide(index)" :class="{'active' : index === indexCurrentSlide}"></div>
      </div>
      <!-- /Buttons -->

    </div>
    <!-- /Content -->

    
  </Section>
</template>

<script>
import slides from '../assets/data/section-home-owners';

export default {
  name: 'SectionHomeOwners',

  data(){
    return{
      slides,

      indexCurrentSlide: 0,
    }
  },

  methods:{
    currentSlide(indice){
      this.indexCurrentSlide = indice;            
    },

    nextSlide(){

      this.indexCurrentSlide++;
      
      if(this.indexCurrentSlide > this.slides.length -1){
        this.indexCurrentSlide = 0;
      }
    },

    startAutoScroll(){

      this.autoScroll = setInterval(() => {
        this.nextSlide();
      }, 3000)
    }
  },

  mounted() {

    this.startAutoScroll()
  }
}
</script>

<style lang="scss" scoped>
section{
  background-image: url('../assets/images/home-parallax-144609983.jpg');
  background-size: cover;
  background-position-y: center;
  color: white;

  .testimonials{
    min-height: 250px;
  }

  .user-image{
    width: 120px;
    height: 120px;
    background-size: cover;
    margin: 10px auto;
    border-radius: 50%;
  }

  p{
    font-size: .9rem;
  }

  .btn-current-slide{
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
  


</style>