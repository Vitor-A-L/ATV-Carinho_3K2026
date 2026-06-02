<script setup>
import { ShoppingCart, Heart, User, Search } from 'lucide-vue-next'
</script>
<template>
  <nav class="navbar">
    <div class="esquerda">
      <h1>Sigma Books </h1>
      <span class="slogan">os livros 10/10</span>
    </div>
    <div class="centro">
      <div class="search-box">


  <input  type="text" placeholder="Pesquisar" >
  <Search />
</div>
      <a href="#">Termos</a>
      <a href="#">Equipe</a>
      <a href="#">Envio</a>
      <a href="#">Devoluções</a>
    </div>
    <div class="direita">
       <span><ShoppingCart /></span>
      <span class="sim"><Heart /></span>
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
  border-bottom: #27ae60 2px solid;


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
  color: #000000;
  font-size: 32px;
}
.slogan{
  margin-left: 10px;
  color: #27ae60;
  font-size: 14px;
  border-left: #27ae60 2px solid;
  width: 65px;
  padding-left: 10px;
}
.centro a{
  text-decoration: none;
  color:rgb(112, 111, 111);
  font-weight: 500;

}
.search-box{
  position: relative;

  display: flex;
  align-items: center;
}

.search-box svg{
  position: absolute;

  left: 315px;
  right: 10px;

  width: 18px;
  height: 18px;

  color: gray;
}

.search-box input{
  padding-left: 25px;



  width: 350px;
  height: 40px;

  border: none;
  border-radius: 8px;

  background: #f3f3f3;
}

.sim{
  border-left: #27ae60 2px solid;
  padding-left: 15px;
  border-right: #27ae60 2px solid;
  padding-right: 15px;
}
svg{
  width: 22px;
  height: 22px;
  cursor: pointer;
  color: green;
}
</style>