<template>
  
  <div class="col">
    <div class="gb-card">
      <img :src="require(`../../assets/images/${partner.image}`)" class="card-img-top" :alt="partner.alt">
    </div>
  </div>

</template>

<script>
export default {
  name: 'PartnersCard',

  props:{
    partner: Object
  }
}
</script>

<style lang="scss" scoped>

</style>