<template>
  <div class="cart">
    <nav-bar class="nav-bar"><div slot="center">购物车({{length}})</div></nav-bar>
    <!-- 商品列表 -->
    <cart-list></cart-list>
    <!-- 底部导航栏 -->
    <cart-bottom-bar></cart-bottom-bar>
  </div>
</template>

<script>
import NavBar from "../../components/common/navbar/NavBar"
import CartList from "./childComps/CartList"
import CartBottomBar from "./childComps/CartBottomBar"

import { mapGetters } from "vuex"

export default {
  name: 'Cart',
  components: {
    NavBar,
    CartList,
    CartBottomBar
  },
  computed: {
    ...mapGetters({
      length:'cartLength',
    })
  }
 
}
</script>

<style  scoped>
.cart{
  height: 100vh;
}
.nav-bar{
  background-color: var(--color-high-text);
  color:#fff;
}
</style>
