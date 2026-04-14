```html
<!DOCTYPE html>
<html lang="pt-br">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Exemplo HTML</title>
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: sans-serif;
    }
    body {
      display: flex;
      flex-direction: column;
      height: 100vh;
    }
    .barra-superior {
      height: 60px;
      background: #333;
      display: flex;
      align-items: center;
      gap: 15px;
      padding: 0 10px;
    }
    #toggleNavBtn {
      background: transparent;
      border: none;
      font-size: 24px;
      color: white;
      cursor: pointer;
    }
    #empresa {
      font-weight: bold;
      font-size: 20px;
      color: white;
    }
    #menu-nav {
      position: fixed;
      left: 0;
      top: 60px;
      width: 150px;
      height: calc(100vh - 60px);
      background: #f4f4f4;
      padding: 10px;
      overflow-y: auto;
      display: none;
    }
    #menu-nav.menu-aberto {
      display: block;
    }
    #menu-nav ul {
      list-style: none;
    }
    #menu-nav li {
      padding: 15px 10px;
      border-bottom: 1px solid #ddd;
    }
    #menu-nav a {
      text-decoration: none;
      color: #333;
    }
    #menu-nav a:hover {
      color: #666;
      font-weight: bold;
    }
    .container {
      margin-left: 0;
      padding: 15px;
      flex: 1;
      overflow-y: auto;
      transition: margin-left 0.3s;
    }
    @media (min-width: 769px) {
      #toggleNavBtn { display: none; }
      #menu-nav { display: block; }
      .container.menu-aberto { margin-left: 150px; }
    }
    @media (max-width: 768px) {
      #menu-nav { width: 260px; }
    }
  </style>
</head>
<body>
  <div class="barra-superior">
    <button id="toggleNavBtn" onclick="toggleNav()">☰</button>
    <span id="empresa">Empresa</span>
  </div>
  <nav id="menu-nav">
    <ul>
      <li><a href="#">Dashboard</a></li>
      <li><a href="#">Vendas</a></li>
      <li><a href="#">Clientes</a></li>
      <li><a href="#">Relatórios</a></li>
      <li><a href="#">Configurações</a></li>
      <li><a href="https://google.com" target="_blank">Link Externo</a></li>
    </ul>
  </nav>  
  <div class="container">
    <h1>Olá, Mundo!</h1>
    <p>Este é um exemplo básico de HTML com um pouco de CSS e JavaScript.</p>
    <br /> <br />
    <img src="./imagem.jpg" alt="Descrição da imagem" style="width: 250px; display: block;">
    <br /> <br />
    <form action="#" method="POST">
      <label for="nome">Nome: </label> <br />
      <input type="text" id="nome" name="nome">
      <button type="submit">Enviar</button> <br />
    </form>
  </div>
  <script>
    const nav = document.getElementById('menu-nav');
    const container = document.querySelector('.container');
    function toggleNav() {
      nav.classList.toggle('menu-aberto');
      container.classList.toggle('menu-aberto');
    }
    function applyResponsive() {
      const isMobile = window.innerWidth <= 768;
      if (!isMobile) {
        nav.classList.add('menu-aberto');
        container.classList.add('menu-aberto');
      } else {
        nav.classList.remove('menu-aberto');
        container.classList.remove('menu-aberto');
      }
    }
    applyResponsive();
    window.addEventListener('resize', applyResponsive);
  </script>
</body>
</html>
```
