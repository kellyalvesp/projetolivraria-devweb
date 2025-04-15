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
          <input type="text" id="pesquisa" />
          <button id="pesquisa-submit">Pesquisar</button>
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
    </main>
  </body>
</template>

<style scoped>

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
hr {
  border: 0;
  border-top: 1px solid #27ae60;
}
.pt1 {
  display: flex;
  margin: 5rem;
}
.pt1 button#autor {
  background-color: white;
  color: #27ae60;
  padding: 10px;
  border-color: #27AE60;
  border-radius: 3px;
}
.pt1 h3 {
  font-weight: bold;
  font-size: 40px;
}
</style>
