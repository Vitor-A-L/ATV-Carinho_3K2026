<script setup>
import { RouterLink } from 'vue-router'
import FacebookIcon from '@iconify-vue/uil/facebook'
import InstagramIcon from '@iconify-vue/uil/instagram'
import TwitterIcon from '@iconify-vue/uil/twitter'
</script>

<template>
  <section class="rodape">
    <div class="redes">
      <h2 style="font-family: 'Playfair Display', serif">Redes Sociais</h2>
      <FacebookIcon height="1em" style="color: #000" />
      <InstagramIcon height="1em" style="color: #000" />
      <TwitterIcon height="1em" style="color: #000" />
    </div>
    <div class="desenvolvedores">
      <h2 style="font-family: 'Playfair Display', serif">Desenvolvido Por</h2>
      <p>Vitor Avanzi Lipinski</p>
      <p>Nicholas Oyafuso</p>
      <p>Rafael Alvez dos Santos</p>
    </div>
    <div class="info">
      <h2 style="font-family: 'Playfair Display', serif">Informações de Contato</h2>
      <a href="">sigma'scoffee@gmail.com</a>
      <RouterLink to="/"><a href="#">Voltar Para o Menu</a></RouterLink>
    </div>
  </section>
  ©Sigma's coffee
</template>

<style scoped>
.rodape {
  align-items: center;
  display: flex;
  flex-wrap: wrap;
   gap: 195px;
position: relative;
  justify-content: center;
  color: #000000;
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  font-size: 14px;
}
</style>
