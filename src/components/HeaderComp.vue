<template>
  <header class="d-flex justify-content-between align-items-center px-5 py-4">
    
    <!-- Logo -->
    <div class="logo">
      <img class="w-100" src="../assets/images/construction_logo.png" alt="Logo">
    </div>

    <!-- Nav bar -->
    <nav class="d-flex">
      <ul class="d-flex mb-0">
        <li v-for="(menuItem, index) in MenuItems" :key="`menuItem-${index}`" class="d-flex align-items-center">
          <a :class="{'active' : menuItem.isActive}" :href="menuItem.href">{{menuItem.name}}</a>
        </li>
      </ul>
      <button type="button" class="btn btn-warning gb-btn">get quote</button>
    </nav>
    <!-- /Nav bar -->

  </header>
</template>

<script>
import MenuItems from '../assets/data/header-nav'

export default {
  name: 'HeaderComp',

  data(){
    return{
      MenuItems
    }
  }
}
</script>

<style lang="scss" scoped>
@import '../assets/style/vars';

header{
  .logo{
    width: 150px;
  }

  li{
    padding: 0 15px;
  }

  a{
    color: #858585;
    text-transform: uppercase;
    font-weight: 200;
    font-size: .8rem;
    display: inline-block;
    &:hover,
    &.active{
      color: $primary-color;
    }
  }

  .gb-btn{
    background-color: $primary-color;
    border-radius: 0%;
    padding: 5px 20px;
    color: #858585;
    font-size: .8rem;
    text-transform: uppercase;
    font-weight: 200;
    &:hover{
      background-color: $secondary-color;
      color: white;
      border: 1px solid $secondary-color;
    }
  }
}
</style>