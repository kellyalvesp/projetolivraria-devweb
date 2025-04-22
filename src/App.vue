<script setup></script>

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
            <input type="" placeholder="Pesquisar" />
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
            <li><span class="fa-solid fa-cart-shopping"></span></li>
            <li><span class="fa-solid fa-heart"></span></li>
            <li><span class="fa-solid fa-user"></span></li>
          </ul>
        </div>
      </nav>
      <hr />
    </header>
    <main>
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
        <ul>
          <div class="cima">
            <li>
              <a href="#"><img src="/public/images/9781982185824 2.png" alt="" /></a>
              <h4>Chain of Iron: Volume 2</h4>
              <p>Cassandra Clare</p>
              <p>R$23.24</p>
              <button><span class="fa-solid fa-cart-shopping"></span>Comprar</button>
            </li>
            <li>
              <a href="#"><img src="/public/images/9781982185824 2(1).png" alt="" /></a>
              <h4>Chain of Thorns</h4>
              <p>Cassandra Clare</p>
              <p>R$23.24</p>
              <span class="fa-regular fa-heart"></span>
              <button><span class="fa-solid fa-cart-shopping"></span>Comprar</button>
            </li>
            <li>
              <a href="#"><img src="/public/images/9781982185824 2(2).png" alt="" /></a>
              <h4>City of Fallen Angels</h4>
              <p>Cassandra Clare</p>
              <p>R$13.94</p>
              <span class="fa-regular fa-heart"></span>
              <button><span class="fa-solid fa-cart-shopping"></span>Comprar</button>
            </li>
            <li>
              <a href="#"><img src="/public/images/9781982185824 2(3).png" alt="" /></a>
              <h4>Nona the Ninth</h4>
              <p>Cassandra Clare</p>
              <p>R$16.84</p>
              <span class="fa-regular fa-heart"></span>
              <button><span class="fa-solid fa-cart-shopping"></span>Comprar</button>
            </li>
          </div>
          <div class="baixo">
            <li>
              <a href="#"><img src="/public/images/9781982185824 2(4).png" alt="" /></a>
              <h4>Harlem Shuffle</h4>
              <p>Colson Whitehead</p>
              <p>R$26.92</p>
              <button><span class="fa-solid fa-cart-shopping"></span>Comprar</button>
            </li>
            <li>
              <a href="#"><img src="/public/images/9781982185824 2(5).png" alt="" /></a>
              <h4>Two Old Women</h4>
              <p>Velma Wallis</p>
              <p>R$13.95</p>
              <span class="fa-regular fa-heart"></span>
              <button><span class="fa-solid fa-cart-shopping"></span>Comprar</button>
            </li>
            <li>
              <a href="#"><img src="/public/images/9781982185824 2(6).png" alt="" /></a>
              <h4>Carrie Soto Is Back</h4>
              <p>Taylor Jenkins Reid</p>
              <p>R$26.04</p>
              <span class="fa-regular fa-heart"></span>
              <button><span class="fa-solid fa-cart-shopping"></span>Comprar</button>
            </li>
            <li>
              <a href="#"><img src="/public/images/9781982185824 2(7).png" alt="" /></a>
              <h4>Book Lovers</h4>
              <p>Emily Henry</p>
              <p>R$15.81</p>
              <span class="fa-regular fa-heart"></span>
              <button><span class="fa-solid fa-cart-shopping"></span>Comprar</button>
            </li>
          </div>
        </ul>
      </div>
    </main>
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
}
.icones li span {
  color: #27ae60;
}
.pesquisa input {
  padding: 10px 60px 10px 10px;
  margin: 1vw 2px 0 2px;
  background-color: #f1f1f1;
  border: none;
}
hr {
  border: 0;
  border-top: 1px solid #27ae60;
}
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
</style>
