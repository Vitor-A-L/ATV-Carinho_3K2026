<script setup>
import FacebookIcon from '@iconify-vue/uil/facebook'
import InstagramIcon from '@iconify-vue/uil/instagram'
import TwitterIcon from '@iconify-vue/uil/twitter'
</script>

<template>
  <section class="rodape">
    <div class="redes">
      <h2 style="font-family: 'Playfair Display', serif">Redes Sociais</h2>
      <FacebookIcon height="3em" style="color: #000;  margin-right: 20px; margin-top: 17px;" />
      <InstagramIcon height="3em" style="color: #000;  margin-right: 20px;" />
      <TwitterIcon height="3em" style="color: #000;" />
    </div>
    <div class="desenvolvedores">
      <h2 style="font-family: 'Playfair Display', serif">Desenvolvedores</h2>
      <p>- Vitor Avanzi Lipinski -</p>
      <p>- Nicholas Oyafuso -</p>
      <p>- Rafael Alvez dos Santos -</p>
    </div>
    <div class="info">
      <h2 style="font-family: 'Playfair Display', serif">Informações de Contato</h2>
      <a href="mailto:sigma'scoffee@gmail.com">sigma'scoffee@gmail.com</a>
      <p>Tel:+55 47 9922-4519</p>
    </div>
  </section>
  <p class="direitos">©Sigma's coffee</p>
</template>

<style scoped>
.rodape {
  margin-top: -80px;
  display: flex;
  justify-content: space-around;
  align-items: flex-start;
  flex-wrap: wrap;
  padding: 40px 20px;
  width: 100%;
  color: #000;
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  font-size: 14px;
}
.direitos{

text-align: center;
font-weight: bolder;
font-size: 20px;
}
h2{
  font-size: 32px;

}
.desenvolvedores p{
  margin-top: 10px;
  font-weight: lighter;
  font-size: 25px;
  font-style: italic;
}

.info a{
  text-decoration: none;
  color: #000;
  font-size: 20px;
  font-style: italic;
 /* margin-top: 20px;  não sei porque náo funciona o margin aqui*/

}
.info p{
  margin-top: 10px;
  font-size: 20px;

}
</style>
