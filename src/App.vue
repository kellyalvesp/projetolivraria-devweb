<script setup>
import { ref, computed } from 'vue'

const mostrarCarrinho = ref(false)

function abrirCarrinho() {
  mostrarCarrinho.value = true
}

function voltarParaHome() {
  mostrarCarrinho.value = false
}

const contador = ref(1)
const precoUnitario = 23.24
const total = computed(() => {
  return (contador.value * precoUnitario).toFixed(2).replace('.', ',')
})
function incrementar() {
  contador.value++
}
function decrementar() {
  contador.value--
}
</script>

<template>
  <body>
    <header>
      <nav>
        <div class="sup-esquerdo">
          <div class="logo">
            <h1>
              <a href="index.html"><img src="/images/logo.png" alt="" /></a>
            </h1>
            <div class="linha-vertical"></div>
            <h2>
              <a href="index.html"><img src="/images/aprleitura.png" alt="" /></a>
            </h2>
          </div>
          <div class="pesquisa">
            <input type="text" placeholder="Pesquisar" />
          </div>
        </div>
        <div class="navegacao">
          <ul class="abas">
            <li><a href="#">Termos</a></li>
            <li><a href="#">Equipe</a></li>
            <li><a href="#">Envios</a></li>
            <li><a href="#">Devoluções</a></li>
          </ul>
        </div>
        <div class="icons">
          <ul class="icones">
            <li @click="abrirCarrinho"><span class="fa-solid fa-cart-shopping"></span></li>
            <div class="linha-vicon"></div>
            <li><span class="fa-solid fa-heart"></span></li>
            <div class="linha-vicon"></div>
            <li><span class="fa-solid fa-user"></span></li>
          </ul>
        </div>
      </nav>
      <hr />
    </header>
    <main v-if="!mostrarCarrinho">
      <div class="pt1">
        <div class="lado-esquerdo">
          <button id="autor">Autor de Abril</button>
          <h3>Eric-Emanuel Schmitt</h3>
          <p>
            Eric-Emmanuel Schmitt has been awarded more than 20 literary prizes and distinctions,
            and in 2001 he received the title of Chevalier des Arts et des Lettres. His books have
            been translated into over 40 languages.
          </p>
          <button id="acessa-pagina">Acessar página do livro</button>
        </div>
        <div class="img">
          <a href="#"><img src="/public/images/image.png" alt="" /></a>
        </div>
      </div>
      <hr />
      <div class="categorias">
        <ul class="ana">
          <li><span class="fa-solid fa-truck"></span>Frete grátis para SC</li>
          <div class="linha-vertical2"></div>
          <li><span class="fa-solid fa-star"></span>Livros recomendados</li>
          <div class="linha-vertical2"></div>
          <li><span class="fa-solid fa-book-open"></span>Mais vendidos</li>
        </ul>
      </div>
      <hr />
      <div class="lancamentos">
        <h3>Lançamentos</h3>
        <div class="livros">
          <ul>
            <div class="cima">
              <li>
                <a href="#"><img src="/public/images/9781982185824 2.png" alt="" /></a>
                <h4>Chain of Iron: Volume 2</h4>
                <p class="autor">Cassandra Clare</p>
                <p class="preco">R$23.24</p>
                <button><span class="fa-solid fa-cart-shopping"></span>Comprar</button>
              </li>
              <li>
                <a href="#"><img src="/public/images/9781982185824 2(1).png" alt="" /></a>
                <h4>Chain of Thorns</h4>
                <p class="autor">Cassandra Clare</p>
                <p class="preco">R$23.24 <span class="fa-regular fa-heart"></span></p>

                <button><span class="fa-solid fa-cart-shopping"></span>Comprar</button>
              </li>
              <li>
                <a href="#"><img src="/public/images/9781982185824 2(2).png" alt="" /></a>
                <h4>City of Fallen Angels</h4>
                <p class="autor">Cassandra Clare</p>
                <p class="preco">R$13.94 <span class="fa-regular fa-heart"></span></p>

                <button><span class="fa-solid fa-cart-shopping"></span>Comprar</button>
              </li>
              <li>
                <a href="#"><img src="/public/images/9781982185824 2(3).png" alt="" /></a>
                <h4>Nona the Ninth</h4>
                <p class="autor">Cassandra Clare</p>
                <p class="preco">R$16.84 <span class="fa-regular fa-heart"></span></p>
                <button><span class="fa-solid fa-cart-shopping"></span>Comprar</button>
              </li>
            </div>
            <div class="baixo">
              <li>
                <a href="#"><img src="/public/images/9781982185824 2(4).png" alt="" /></a>
                <h4>Harlem Shuffle</h4>
                <p class="autor">Colson Whitehead</p>
                <p class="preco">R$26.92</p>
                <button><span class="fa-solid fa-cart-shopping"></span>Comprar</button>
              </li>
              <li>
                <a href="#"><img src="/public/images/9781982185824 2(5).png" alt="" /></a>
                <h4>Two Old Women</h4>
                <p class="autor">Velma Wallis</p>
                <p class="preco">R$13.95 <span class="fa-regular fa-heart"></span></p>
                <button><span class="fa-solid fa-cart-shopping"></span>Comprar</button>
              </li>
              <li>
                <a href="#"><img src="/public/images/9781982185824 2(6).png" alt="" /></a>
                <h4>Carrie Soto Is Back</h4>
                <p class="autor">Taylor Jenkins Reid</p>
                <p class="preco">R$26.04 <span class="fa-regular fa-heart"></span></p>

                <button><span class="fa-solid fa-cart-shopping"></span>Comprar</button>
              </li>
              <li>
                <a href="#"><img src="/public/images/9781982185824 2(7).png" alt="" /></a>
                <h4>Book Lovers</h4>
                <p class="autor">Emily Henry</p>
                <p class="preco">R$15.81 <span class="fa-regular fa-heart"></span></p>
                <button><span class="fa-solid fa-cart-shopping"></span>Comprar</button>
              </li>
            </div>
          </ul>
        </div>
      </div>
    </main>
    <section class="carrinho" v-else>
      <h5>Carrinho</h5>
      <ul class="partes">
        <li class="titulo-car">Título</li>
        <li>Quantidade</li>
        <li class="subtotal">Subtotal</li>
      </ul>
      <div class="linha-horizontal"></div>
      <div class="livro1">
        <div class="imagem">
          <img src="/public/images/volume2.png" alt="" />
        </div>
        <div class="maior-info">
          <div class="info">
            <h6>Chain of Iron: Volume 2</h6>
            <p class="nome-autor">Cassandra Clare</p>
            <p class="preco-carrinho">R$23,24</p>
          </div>
          <div class="botao-preco">
            <div class="botao">
              <button class="contador" v-on:click="incrementar">+</button>
              <p>{{ contador }}</p>
              <button @click="decrementar">-</button>
            </div>
            <p class="preco-total">R${{ total }}</p>
          </div>
        </div>
      </div>
      <div class="linhahor-livro"></div>
      <div class="livro2">
        <div class="imagem">
          <img src="/public/images/volume2.png" alt="" />
        </div>
        <div class="maior-info">
          <div class="info">
            <h6>Chain of Iron: Volume 2</h6>
            <p class="nome-autor">Cassandra Clare</p>
            <p class="preco-carrinho">R$23,24</p>
          </div>
          <div class="botao-preco">
            <div class="botao">
              <button v-on:click="incrementar">+</button>
              <p>{{ contador }}</p>
              <button @click="decrementar">-</button>
            </div>
            <p class="preco-total">R${{ total }}</p>
          </div>
        </div>
      </div>
      <div class="linhahor-livro"></div>
      <button class="voltar" @click="voltarParaHome">Voltar para loja</button>
      <div class="div-maiorct">
        <div class="cupom-maior">
          <div class="cupom">
            <input type="text" placeholder="Código de cupom" />
          </div>
          <div class="inserir">
            <button class="insert">Inserir cupom</button>
          </div>
        </div>
        <div class="tabela">
          <h2>Total da compra</h2>
          <ul>
            <li class="linha">
              <span>Produtos:</span>
              <span>R$175</span>
            </li>
            <div class="linha-tabela"></div>
            <li class="linha">
              <span>Frete:</span>
              <span>Grátis</span>
            </li>
            <div class="linha-tabela"></div>
            <li class="linha total">
              <span>Total:</span>
              <span>R$175</span>
            </li>
          </ul>
          <button class="pagamento">Ir para pagamento</button>
        </div>
      </div>
    </section>
    <footer>
      <div class="container">
        <div class="esquerda">
          <p>IFbooks</p>
          <ul class="redes-sociais">
            <li><span class="fa-brands fa-square-facebook"></span></li>
            <li><span class="fa-brands fa-square-instagram"></span></li>
            <li><span class="fa-brands fa-square-twitter"></span></li>
          </ul>
        </div>
        <div class="direita">
          <p>Contato</p>
          <ul class="contato">
            <li><span class="fa-solid fa-phone"></span>+55 47 40045263</li>
            <li><span class="fa-solid fa-clock"></span>8h às 23h - Seg a Sex</li>
            <li><span class="fa-solid fa-envelope"></span>contato@ifbooks.com</li>
          </ul>
          <a class="pagamentos" href="index.html"
            ><img src="/public/images/ways to pay.png" alt=""
          /></a>
        </div>
      </div>
      <div class="direitos">
        <p>© Alguns direitos reservados. IFbooks 2025.</p>
      </div>
    </footer>
  </body>
</template>

<style scoped>
body {
  font-family:
    'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif;
}
a {
  text-decoration: none;
}
.abas,
.icones {
  list-style: none;
  padding: 0;
  margin: 0;
}
nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin: 10px 50px 10px 50px;
  padding: 10px 20px;
  flex-wrap: wrap;
}

.logo {
  display: flex;
  padding: 0;
  margin: 0 10px 0;
  align-items: center;
  gap: 10px;
  color: #27ae60;
}
.linha-vertical {
  height: 40px;
  border-left: 2px solid;
}
.abas {
  display: flex;
  padding: 0;
  margin: 0;
  display: flex;
  gap: 20px;
}
.abas li a {
  color: #7b7881;
}
.sup-esquerdo {
  display: flex;
}
.icones {
  display: flex;
  padding: 0;
  margin: 0;
  gap: 20px;
  font-size: larger;
}
.icones li span {
  color: #27ae60;
}
.linha-vicon {
  color: #27ae60;
  height: 20px;
  border-left: 2px solid;
}
.pesquisa input {
  padding: 10px 60px 10px 10px;
  margin: 0 2px 0 2px;
  background-color: #f1f1f1;
  border: none;
}
hr {
  border: 0;
  border-top: 1px solid #27ae60;
}

/*============================
        PRIMEIRA PAGINA
=============================*/

.pt1 {
  display: flex;
  margin: 5vw 10vw 2vw 10vw;
}
.pt1 button#autor {
  background-color: white;
  color: #27ae60;
  padding: 10px;
  border-color: #27ae60;
  border-radius: 3px;
}
.pt1 h3 {
  font-weight: bold;
  font-size: 40px;
}
button#acessa-pagina {
  color: white;
  background-color: #27ae60;
  border-color: #27ae60;
  font-size: 17px;
  padding: 10px 40px 10px 40px;
  margin: 3rem 0 0 0;
}
.pt1 p {
  color: #4d4c4c;
}
.pt1 img {
  margin: 0 60px 0 80px;
}
.linha-vertical2 {
  height: 40px;
  border-left: 2px solid;
  color: #7b7881;
}
.categorias,
.ana {
  color: #382c2c;
  list-style: none;
  margin: 3vw 0 3vw 0;
}
.ana {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin: 0 10vw 0 10vw;
  padding: 0 0 0 10px;
  font-size: 25px;
}
.ana span {
  padding: 0 25px 0 0;
}
.lancamentos h3 {
  font-size: 2rem;
  margin: 3vw 10vw 0 10vw;
}
.lancamentos ul {
  list-style: none;
}
.lancamentos div.cima {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin: 2vw 6.7vw 0 6.7vw;
  padding: 0 20px 0 20px;
}
.lancamentos div.baixo {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin: 2vw 6.7vw 0 6.7vw;
  padding: 3vw 20px 0 20px;
}
.livros button {
  background-color: #27ae60;
  color: white;
  border: none;
  border-radius: 3%;
  padding: 15px 100px 15px 100px;
  font-size: 1rem;
}
.livros h4 {
  font-size: 1.5rem;
  margin: 20px 0 2px 0;
}
.livros p.autor {
  color: #7b7881;
}
.livros p.preco {
  font-weight: bold;
  font-size: 1.3rem;
  margin: 0 0 25px 0;
  justify-content: space-between;
  display: flex;
}

/*============================
          SEGUNDA PAGINA
=============================*/
.linha-horizontal {
  border-top: 2px solid #27ae60;
  margin: 8px 0 25px 0;
}
.carrinho {
  margin: 10vw 5vw 3vw 5vw;
}
.carrinho h5 {
  color: #27ae60;
  font-size: 1.8vw;
}
.carrinho ul.partes {
  list-style: none;
  display: flex;
  font-weight: bold;
  margin: 3vw 0 0 0;
  font-size: 1.5rem;
}
.carrinho li.titulo-car {
  margin: 0 50vw 0 0;
}
.carrinho li.subtotal {
  margin: 0 0 0 14vw;
}
.livro1 {
  display: flex;
}
.livro2 {
  display: flex;
  margin: 2vw 0 2vw 0;
}
.botao-preco {
  display: flex;
  align-items: center;
}
.maior-info {
  display: flex;
}
.info {
  margin: 0 37.5vw 0 1vw;
}
.preco-total {
  margin: 0 0 0 10vw;
}
.linhahor-livro {
  border-top: 1px solid #bdbdbd;
  margin: 2vw 0 0 0;
}
h6 {
  font-size: 19px;
  color: #382c2c;
  margin: 0 0 0.7vw 0;
}
.nome-autor {
  font-size: 13px;
  margin: 0 0 0.7vw 0;
  color: #4f4c57;
}
.preco-carrinho {
  font-weight: bold;
  font-size: 16.5px;
}
.preco-total {
  font-weight: bold;
  margin: 0 0 0 16.3vw;
}
.botao {
  border: 1.7px solid black;
  display: flex;
  padding: 0.5vw 1.2vw 0.5vw 1.2vw;
}
button {
  background-color: #ffffff;
  border: #ffffff;
}
.voltar {
  border: 1.7px solid black;
  padding: 0.8vw 1.5vw 0.8vw 1.5vw;
  border-radius: 4%;
  margin: 3vw 0 0 0;
  font-size: 1rem;
}
.imagem {
  margin: 0 0 0 2vw;
}
.cupom input {
  border: 1.7px solid black;
  border-radius: 3%;
  background-color: #ffffff;
  margin: 3.5vw 0 0 0;
  font-size: 1rem;
  padding: 1vw 4vw 1vw 1vw;
}
.cupom-maior {
  display: flex;
}
.inserir {
  margin: 3.5vw 1vw 3.5vw 1vw;
}
button.insert {
  background-color: #27ae60;
  border: 1.7px solid #28a651;
  border-radius: 3%;
  color: #ffffff;
  font-size: 1rem;
  padding: 1vw 3vw 1vw 3vw;
}
.div-maiorct {
  display: flex;
}
.tabela {
  border: 2px solid #000000;
  border-radius: 4px;
  margin: 3.5vw 0 0 25vw;
  width: 470px;
  height: 355px;
  top: 1074px;
  left: 841px;
  display: flex;
  flex-direction: column;
  gap: 30px;
  align-items: center;
  justify-content: center;
}

.tabela ul {
  width: 80%;
}

.linha {
  flex: 1;
  display: flex;
  justify-content: space-between;
  padding: 4px 0;
}
.total {
  font-weight: bold;
}
.linha-tabela {
  border-top: 1px solid #bdbdbd;
  margin: 2vw 0 0 0;
}
.pagamento {
  background-color: #27ae60;
  border: 1.7px solid #28a651;
  border-radius: 3%;
  color: #ffffff;
  font-size: 1rem;
  padding: 1vw 2vw 1vw 2vw;
  margin: 0 0 1vw 0;
}

/*============================
          FOOTER
=============================*/

footer {
  background-color: #28a651;
  margin: 10vw 0 0 0;
  padding: 40px 60px 10px;
}
.esquerda,
.direita {
  display: flex;
  flex-direction: column;
  gap: 15px;
}
.esquerda ul {
  list-style: none;
  display: flex;
}
.esquerda {
  color: #ffffff;
  padding: 0 5vw 5vw 5vw;
}
.esquerda p {
  font-size: 1.2rem;
  margin: 0;
}
.direita {
  padding: 0 5vw 5vw 5vw;
}
.direita p {
  color: #ffffff;
  font-size: 1.2rem;
  margin: 0 0 2px 0;
}
.direita ul {
  color: #ffffffcc;
  list-style: none;
}
.direita span {
  padding: 0 10px 0 0;
}
.container {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  flex-wrap: wrap;
}
.redes-sociais {
  display: flex;
  gap: 10px;
  list-style: none;
  padding: 0;
}
.redes-sociais li span {
  font-size: 1.7rem;
}
.contato {
  list-style: none;
  padding: 0;
  display: flex;
  flex-direction: column;
  gap: 8px;
}
.contato li span {
  margin-right: 8px;
}
.pagamentos img {
  margin-top: 10px;
  height: 30px;
}
.direitos {
  text-align: center;
  border-top: 2px solid rgba(255, 255, 255, 0.705);
  margin-top: 30px;
  padding-top: 15px;
  font-size: 0.9rem;
  opacity: 0.8;
}
.direitos p {
  color: #ffffff99;
}
</style>
