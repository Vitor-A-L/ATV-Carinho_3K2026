<script setup>
import NavBar from '@/components/navBar.vue'
import { ShoppingCart } from 'lucide-vue-next'
import { RouterLink } from 'vue-router'
const subtotal = 'R$146,32'
const shipping = 'R$0,00'
const total = 'R$146,32'
const cartItems = [
  {
    id: 1,
    titulo: 'Vanila Ice',
    descricao: 'Super Fresh',
    imagem: '/vanila-ice.png',
    valor: 'R$29,99',
    quantidade: 2,
    subtotal: 'R$59,98'
  }
]
</script>

<template>
  <NavBar />

  <section class="cart">
    <div class="container">

      <div v-if="cartItems.length === 0" class="empty-cart">
        <ShoppingCart />

        <h2>Seu carrinho está vazio</h2>

        <p>
          Adicione alguns cafés para começar seu pedido.
        </p>

        <RouterLink to="/" class="shop-btn">
          Explorar Cafés
        </RouterLink>
      </div>

      <div v-else>

        <h1>Carrinho</h1>

        <div class="table-header">
          <span>Título</span>
          <span>Quantidade</span>
          <span>Subtotal</span>
        </div>

        <div
          v-for="item in cartItems"
          :key="item.id"
          class="cart-item"
        >
          <div class="product">
            <img :src="item.imagem" :alt="item.titulo">

            <div>
              <h3>{{ item.titulo }}</h3>
              <p>{{ item.descricao }}</p>
              <span>{{ item.valor }}</span>
            </div>
          </div>

          <div class="quantity">
            <button>-</button>
            <span>{{ item.quantidade }}</span>
            <button>+</button>
          </div>

          <h4>{{ item.subtotal }}</h4>
        </div>

        <RouterLink to="/" class="back">
          Voltar para loja
        </RouterLink>
   <div class="bottom">

 

  <div class="summary">
    <h3>Total da Compra</h3>

    <div class="line">
      <span>Produtos:</span>
      <span>{{ subtotal }}</span>
    </div>

    <div class="line">
      <span>Frete:</span>
      <span>{{ shipping }}</span>
    </div>

    <div class="line total">
      <span>Total:</span>
      <span>{{ total }}</span>
    </div>

    <button class="checkout">
      Ir para o pagamento
    </button>
  </div>
</div>
</div>
      </div>

  </section>
</template>

<style scoped>
.bottom{
  display: flex;
  justify-content: space-between;
  align-items: flex-start;

  margin-top: 50px;
  width: 100%;
}

.summary{
  width: 350px;
  margin-left: auto; /* empurra para a direita */
}

.summary h3{
  color: white;
  font-size: 2rem;
  font-family: "Playfair Display", serif;
  margin-bottom: 30px;
}

.line{
  display: flex;
  justify-content: space-between;
  padding: 16px 0;
  color: #b9b9b9;
}

.total{
  border-top: 1px solid rgba(201,138,75,.25);
  margin-top: 10px;
  padding-top: 20px;

  color: white;
  font-size: 1.2rem;
  font-weight: 700;
}

.checkout{
  width: 100%;
  margin-top: 30px;

  padding: 14px;

  border: none;
  border-radius: 8px;

  background: #c98a4b;
  color: white;

  font-size: 1rem;
  font-weight: 600;

  cursor: pointer;
  transition: .3s;
}

.checkout:hover{
  background: #d89a5b;
}
.cart{
    min-height:100vh;
    background:#0f0b08;
    color:white;
    padding:120px 0;
}

.container{
    width:80%;
    margin:auto;
}

.cart h1{
    color:#c98a4b;
    margin-bottom:40px;
    font-family:"Playfair Display", serif;
}

.table-header{
    display:grid;
    grid-template-columns:2fr 1fr 1fr;
    padding-bottom:15px;
    border-bottom:1px solid #c98a4b;
    color:#c98a4b;
}

.cart-item{
    display:grid;
    grid-template-columns:2fr 1fr 1fr;
    align-items:center;
    padding:30px 0;
    border-bottom:1px solid #2a211b;
}

.product{
    display:flex;
    gap:15px;
}

.product img{
    width:70px;
    height:90px;
    object-fit:cover;
    border-radius:8px;
}

.product h3{
    margin-bottom:5px;
}

.product p{
    color:#999;
    font-size:.85rem;
}

.quantity{
    display:flex;
    gap:10px;
    align-items:center;
}

.quantity button{
    width:35px;
    height:35px;
    border:none;
    background:#1b120d;
    color:white;
    cursor:pointer;
}

.back{
    display:inline-block;

    margin-top:30px;
    padding:12px 20px;

    background:transparent;
    border:1px solid #c98a4b;

    color:white;
    text-decoration:none;
}

.empty-cart{
    min-height:65vh;

    display:flex;
    flex-direction:column;
    justify-content:center;
    align-items:center;

    text-align:center;
}

.empty-cart svg{
    width:90px;
    height:90px;

    color:#c98a4b;

    margin-bottom:20px;
}

.empty-cart h2{
    color:white;
    font-size:2.2rem;

    margin-bottom:10px;

    font-family:"Playfair Display", serif;
}

.empty-cart p{
    color:#999;
    max-width:350px;
    line-height:1.6;
}

.shop-btn{
    margin-top:25px;

    padding:14px 28px;

    background:#c98a4b;
    color:white;

    text-decoration:none;
    border-radius:8px;
}
</style>
