<script setup>
defineProps({
  titulo: { type: String },
  descricao: { type: String },
  imagem: { type: String },
  valor: { type: String }
})
import { ShoppingCart } from 'lucide-vue-next'
</script>
<template>
  <nav class="main">
    <div class="coffe">
      <img :src="imagem" alt="title" />
      <h1>{{ titulo }}</h1>
      <h2>{{ descricao }}</h2>
      <p class="desc">{{ valor }}</p>
      <button>
        Adicionar
        <ShoppingCart :size="20" :stroke-width="2.4" />
      </button>
    </div>
  </nav>
</template>

<style scoped>
.main {
  background-color: #e7ddd0;
  border-radius: 6px;
  width: 250px;
  height: 367px;
  font-size: 14px;
  align-items: center;
  position: relative;
}


img {
  width: 420px;
  height: 330px;
  position: absolute;
  top: -60px;
  left: 50%;
  transform: translateX(-50%);
  object-fit: contain;
}


h1 {
  padding-left: 24px;
   margin-top: 230px;
  color: #000000;
  font-family: 'Playfair Display', serif;
  font-size: 2.1rem;
}
h2 {
  padding-left: 24px;
  padding-top: 9px;
  font-size: 12px;
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  color: #4f4c57;
  opacity: 60%;
  font-size: 12px;
}

p {
  padding-left: 24px;
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  font-size: 16px;
  color: #6b4a36;
  font-size: 1.2rem;
  font-weight: bold;
  padding-top: 3px;
}
button {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 15px;
  background-color: #c98a4b;
  width: 250px;
  border-radius: 8px;
  height: 46px;
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  font-weight: bolder;
  font-size: 20px;
  color: #ffffff;
  border: none;
  margin-top: 15px;
  box-shadow: 10px 6px 15px rgba(201, 138, 75, 0.5);
}
</style>
