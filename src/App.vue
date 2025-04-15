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
    </header>
    <main></main>
  </body>
</template>

<style scoped>
/*=============================
            GERAL
==============================*/

html {
  font-family:
    'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif;
  font-size: calc(12px + 0.390625vw);
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
  color: #27AE60;
}
</style>
