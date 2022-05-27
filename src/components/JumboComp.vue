<template>
  <div class="jumbo d-flex justify-content-center align-items-center debug h500">

    <!-- Box -->
    <div class="box">
      <div class="demos debug">
        icona <br>
        <span>testo</span>
      </div>
      <div class="on-sale debug">
        icona <br>
        <span>testo</span>
      </div>
    </div>
    <!-- /Box -->

    <!-- Content Jumbo -->
    <div class="content-jumbo text-center debug">
      <h2>TESTO</h2>
      <h3>TESTO</h3>
      BOTTONE BOTTONE
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
.jumbo{
  position: relative;

  .box{
    position: absolute;
    top: 10px;
    right: 10px;
  }
}
</style>