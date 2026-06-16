
<script setup>
import heroSection from '@/components/heroSection.vue'
import navBar from '@/components/navBar.vue'
import FeaturesSection from '@/components/FeaturesSection.vue'
import dashCoffes from '@/components/dashCoffes.vue'
import footerSection from '@/components/footerSection.vue'

const coffes = [
  { id: 1, titulo:'Vanila Ice', descricao:'Super Fresh' , imagem:'/public/vanila-ice.png', valor: 'R$29.99' },
  { id: 2, titulo:'Expresso', descricao: 'Very Cold', imagem:'/public/expresso-coffee.png', valor: 'R$8.50' },
  { id: 3, titulo:'Cappuccino', descricao: 'Its American Style', imagem:'/public/cappuccino-coffee.png', valor: 'R$23.90' },
  { id: 4, titulo:'Mocha', descricao: 'Relax Vibe', imagem:'/public/mocha-coffee.png', valor: 'R$9.50' },
  { id: 5, titulo:'Americano', descricao: 'Classic Espresso', imagem:'/public/americano-coffee.png', valor: 'R$15.99' },
  { id: 6, titulo:'Affogato', descricao: 'Delicious Dessert', imagem:'/public/affogato-coffee.png', valor: 'R$13.22' },
  { id: 7, titulo:'Macchiatto', descricao: 'Bob Vibes', imagem:'/public/macchiatto-coffee.png', valor: 'R$5.99' },
  { id: 8, titulo:'Irish Coffee', descricao: 'Two Tower', imagem:'/public/irish-coffee.png', valor: 'R$12.00' },
]
</script>

<template>
<navBar></navBar>
<heroSection></heroSection>
<FeaturesSection></FeaturesSection>
<div class="grid">
<dashCoffes
  v-for="coffe in coffes"
  :key="coffe.id"
  :titulo="coffe.titulo"
  :descricao="coffe.descricao"
  :imagem="coffe.imagem"
  :valor="coffe.valor"
></dashCoffes>
</div>
<div class="footer">
<footerSection></footerSection>
</div>
</template>
<style scoped>
.grid{ display: flex;
  align-items: center;
  justify-content: center;
  padding-top: 110px;
  padding-left: 10px;
  display: flex;
  flex-wrap: wrap;
  gap: 165px;
  row-gap: 110px;
}
div.footer{
  margin-top: 110px;
  padding-top: 110px;
  background-color: #c98a4b;
  height: 300px ;
  width: 100%;
}
</style>



