<template>
  <div class='mainTabbar'>
    <tab-bar>
      <tab-bar-item path="/home">
        <template v-slot:item-img>
          <img src="../../../assets/img/tabbar/home.svg">
        </template>
        <template v-slot:item-img-active>
          <img src="../../../assets/img/tabbar/home_active.svg">
        </template>
        <template v-slot:item-title>
          首页
        </template>
      </tab-bar-item>
      <tab-bar-item path="/category">
        <template v-slot:item-img>
          <img src="../../../assets/img/tabbar/category.svg">
        </template>
         <template v-slot:item-img-active>
          <img src="../../../assets/img/tabbar/category_active.svg">
        </template>
        <template v-slot:item-title>
          分类
        </template>
      </tab-bar-item>

      <tab-bar-item path="/cart">
        <template v-slot:item-img>
          <img src="../../../assets/img/tabbar/shopcart.svg">
        </template>
         <template v-slot:item-img-active>
          <img src="../../../assets/img/tabbar/shopcart_active.svg">
        </template>
         <template v-slot:item-title>
          购物车
        </template>
      </tab-bar-item>

      <tab-bar-item path="/profile">
        <template v-slot:item-img>
          <img src="../../../assets/img/tabbar/profile.svg">
        </template>
         <template v-slot:item-img-active>
          <img src="../../../assets/img/tabbar/profile_active.svg">
        </template>
        <template v-slot:item-title>
         我的
        </template>
      </tab-bar-item>

    </tab-bar>
  </div>
</template>

<script>

import TabBar from '../../common/tabbar/TabBar.vue'
import TabBarItem from '../../common/tabbar/TabBarItem.vue'

export default {
  components: {
    TabBar,
    TabBarItem
  }
}

</script>


<style scoped>

</style>