<template>
  
  <div class="col">
    <div class="gb-card">
      <img class="img-fluid" :src="require(`../../assets/images/${image.image}`)" :alt="image.alt">
    </div>
  </div>

</template>

<script>
export default {
  name: 'RecentWorkCard',

  props:{
    image: Object
  }
}
</script>

<style lang="scss" scoped>

</style>