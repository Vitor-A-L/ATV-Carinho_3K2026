<script setup>
import { ShoppingCart,  User, Search } from 'lucide-vue-next'
import { RouterLink } from 'vue-router'
import { inject, computed } from 'vue'

const cart = inject('cart', null)

const totalItens = computed(() => {
  if (!cart) return 0
  return cart.cartItems.value.reduce((acc, item) => acc + item.quantidade, 0)
})
</script>
<template>
  <nav class="navbar">
    <div class="esquerda">
      <h1 style="font-family: 'Playfair Display', serif;">Sigma's coffee </h1>
    </div>
    <div class="centro">
      <div class="search-box">
</div>
      <RouterLink to="/"><a href="#">Home</a></RouterLink>
      <a href="#">Menu</a>
      <a href="#">About Us</a>
      <a href="#">Contact</a>
    </div>
    <div class="direita">
       <RouterLink to="/cart" class="cart-link">
  <ShoppingCart />
  <span v-if="totalItens > 0" class="cart-badge">{{ totalItens }}</span>
</RouterLink>
      <span class="sim"><Search /></span>
      <span><User /></span>
    </div>
  </nav>
</template>
<style scoped>
.navbar{
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 20px 60px;
  margin-top: 25px;
}
.esquerda,
.centro,
.direita{
  display: flex;
  align-items: center;
}
.centro{
  gap: 45px;
}
.direita{
  gap: 16px;
}
.esquerda h1{
  color: #ffffff;
  font-size: 32px;
}
.centro a{
  text-decoration: none;
  color:rgb(255, 255, 255);
  font-weight: 500;
}
.search-box{
  position: relative;
  display: flex;
  align-items: center;
}
.sim{
  padding-left: 15px;
  padding-right: 15px;
}
svg{
  width: 22px;
  height: 22px;
  cursor: pointer;
  color: rgb(255, 255, 255);
}
.cart-link{
  position: relative;
  display: flex;
}
.cart-badge{
  position: absolute;
  top: -8px;
  right: -8px;
  background: #c98a4b;
  color: white;
  font-size: 11px;
  font-weight: 700;
  width: 18px;
  height: 18px;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  line-height: 1;
}
</style>
