<template>
  <Section class="py-5">
   

    <!-- Content Top -->
    <div class="top gb-container text-center">
      <span class="text-capitalize fs-4">Trusted Partners</span>
      <div class="false-hr"></div>
      <p class="p-small lh-lg">Lorem ipsum, dolor sit amet consectetur adipisicing elit. Saepe quis in voluptate totam fuga! Recusandae fugiat distinctio debitis qui blanditiis numquam soluta nemo neque assumenda.</p>
    </div>
    <!-- /Content Top -->


    <!-- Content Bottom -->
    <div class="bottom gb-container-big text-center py-5">

      <!-- Cards -->
      <div class="container-fluid">
        <div class="row row-cols-5">
          <PartnersCard 
          v-for="(partnerItem, index) in partners" :key="`partnerItem-${index}`" 
          :partner="partnerItem"
          />
        </div>
      </div>
      <!-- /Cards -->

    </div>
    <!-- /Content Bottom -->


  </Section>
</template>

<script>
import PartnersCard from './section-cards-comps/PartnersCard.vue';
import partners from '../assets/data/section-partners-img'

export default {
    name: "SectionPartners",

    data(){
      return{
        partners
      }
    },

    components: { PartnersCard }
}
</script>

<style lang="scss" scoped>

</style>