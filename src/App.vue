<script setup>
import { ref, provide } from 'vue'

const cartItems = ref([])

function addToCart(produto) {
  const existente = cartItems.value.find(item => item.titulo === produto.titulo)

  if (existente) {
    existente.quantidade++
  } else {
    cartItems.value.push({
      id: Date.now(),
      titulo: produto.titulo,
      descricao: produto.descricao,
      imagem: produto.imagem,
      valor: produto.valor,
      quantidade: 1
    })
  }
}

function updateQuantity(id, novaQuantidade) {
  if (novaQuantidade <= 0) {
    removeItem(id)
    return
  }
  const item = cartItems.value.find(i => i.id === id)
  if (item) item.quantidade = novaQuantidade
}

function removeItem(id) {
  cartItems.value = cartItems.value.filter(i => i.id !== id)
}

provide('cart', { cartItems, addToCart, updateQuantity, removeItem })
</script>

<template>
  <router-view />
</template>
