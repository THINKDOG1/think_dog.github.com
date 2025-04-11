<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Think Dog</title>
  <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap" rel="stylesheet">
  <script src="https://cdn.jsdelivr.net/npm/qrcode/build/qrcode.min.js"></script>
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: 'Roboto', sans-serif;
    }
    body {
      background-color: #121212;
      color: #f0f0f0;
      transition: background-color 0.3s, color 0.3s;
    }
    body.light {
      background-color: #ffffff;
      color: #121212;
    }
    header {
      position: fixed;
      top: 0;
      width: 100%;
      background-color: rgba(0, 0, 0, 0.8);
      color: white;
      padding: 1rem;
      z-index: 1000;
      display: flex;
      justify-content: space-between;
      align-items: center;
    }
    .logo {
      height: 50px;
    }
    .menu-icon {
      cursor: pointer;
      font-size: 2rem;
    }
    .sidebar {
      position: fixed;
      top: 0;
      right: -250px;
      width: 250px;
      height: 100%;
      background-color: #1f1f1f;
      transition: right 0.3s;
      z-index: 999;
      padding: 2rem 1rem;
    }
    .sidebar.show {
      right: 0;
    }
    .sidebar ul {
      list-style: none;
    }
    .sidebar ul li {
      margin: 1rem 0;
    }
    main {
      padding: 6rem 2rem 2rem;
      max-width: 1000px;
      margin: 0 auto;
    }
    .img-box img {
      max-width: 100%;
      border-radius: 1rem;
      transition: transform 0.3s ease;
    }
    .img-box img:hover {
      transform: rotateY(10deg);
    }
    .description, .services, .feedback, .avaliar {
      margin: 2rem 0;
    }
    .quote {
      background-color: #333;
      padding: 1rem;
      border-radius: 8px;
      margin-top: 1rem;
    }
    .compra {
      display: none;
      margin-top: 2rem;
    }
    .qr-container {
      margin-top: 1rem;
    }
    button {
      padding: 0.7rem 1.2rem;
      border: none;
      border-radius: 5px;
      background-color: #8B4513;
      color: white;
      cursor: pointer;
      margin-top: 1rem;
    }
    input[type="text"] {
      padding: 0.5rem;
      margin-right: 0.5rem;
    }
    .feedback p {
      background: #2c2c2c;
      padding: 0.5rem 1rem;
      margin: 0.5rem 0;
      border-left: 4px solid #8B4513;
    }
  </style>
</head>
<body>
  <header>
    <img src="https://i.imgur.com/O9uEhRB.png" alt="Think Dog Logo" class="logo" />
    <div class="menu-icon" onclick="toggleSidebar()">☰</div>
  </header>

  <div class="sidebar" id="sidebar">
    <ul>
      <li><a href="#inicio">Início</a></li>
      <li><a href="#servicos">Serviços</a></li>
      <li><a href="#comprar">Comprar</a></li>
      <li><a href="https://chat.whatsapp.com/EHBXUktjBP78tAGb1OpL4s" target="_blank">Suporte</a></li>
      <li><button onclick="toggleTheme()" id="themeToggle">Tema Claro</button></li>
    </ul>
  </div>

  <main>
    <section id="inicio">
      <div class="img-box">
        <img src="https://i.imgur.com/iauKggv.jpeg" alt="Cachorro Fofo" />
      </div>
      <div class="description">
        <h2>Bem-vindo à Think Dog</h2>
        <p>Transformamos a comunicação entre humanos e cachorros. Com apoio da Fundação CDL, oferecemos sessões onde nossos profissionais traduzem os pensamentos dos cães para seus donos. Cada sessão custa <strong>R$190,90</strong>.</p>
        <div class="quote">"Seu doguinho tem muito a dizer. Nós traduzimos para você entender."</div>
      </div>
    </section>

    <section id="servicos" class="services">
      <h3>Serviço Think Dog</h3>
      <p>• Sessões com tradutores especializados em comportamento canino.<br>• Cada sessão: <strong>R$109,90</strong></p>
      <button onclick="mostrarCompra()">Comprar Sessão</button>
    </section>

    <section class="compra" id="compra">
      <h3>Finalizar Compra</h3>
      <input type="text" id="cupom" placeholder="Digite o código de desconto">
      <button onclick="aplicarDesconto()">Confirmar Cupom</button>
      <div id="descontoInfo"></div>
      <button onclick="gerarQR()">Pagamento</button>
      <div id="qrcode" class="qr-container"></div>
      <div id="timer"></div>
    </section>

    <section class="feedback">
      <h3>Feedbacks</h3>
      <p>"João marcos:
      Nunca entendi tanto meu doguinho, obrigado Think Dog!"</p>
      <p>"mattheus pereira: Achei que era brincadeira, mas fiquei emocionado com a sessão."</p>
    </section>

    <section class="avaliar">
      <h3>Avalie nosso site</h3>
      <input type="text" placeholder="Digite seu feedback..." />
      <button>Enviar</button>
    </section>
  </main>

<section id="suporte" style="margin-top: 3rem; padding: 2rem; background-color: #1f1f1f; border-radius: 10px; text-align: center;">
  <h2 style="margin-bottom: 1rem;">Suporte Think Dog</h2>
  <p style="margin-bottom: 1rem;">Escaneie o QR code abaixo e entre no nosso grupo de suporte no WhatsApp!</p>
  <img src="https://i.imgur.com/vYRaF4M.png" alt="QR Code Suporte" style="width: 180px; border-radius: 10px; box-shadow: 0 0 10px rgba(0,0,0,0.5);" />
  <p style="margin-top: 1rem;">
    Ou clique direto no link: <br>
    <a href="https://chat.whatsapp.com/EHBXUktjBP78tAGb1OpL4s" target="_blank" style="color: #8B4513; text-decoration: underline;">
      Acessar grupo de suporte
    </a>
  </p>
</section>

<!-- Adicione este trecho antes da tag </body> -->
<footer style="background-color:#1f1f1f; padding: 1rem; text-align: center; color: #aaa; margin-top: 2rem; font-size: 0.9rem;">
  Think Dog Tecnologia e Comportamento Animal LTDA<br>
  CNPJ: 12.345.678/0001-99<br>
  Todos os direitos reservados think dog © 2025
</footer>
<!-- BOTÃO DE ACESSIBILIDADE -->
<div id="acessibilidade-btn" onclick="toggleAcessibilidade()" title="Acessibilidade">
  <img src="https://i.imgur.com/xzDXTxW.png" alt="Acessibilidade" />
</div>

<!-- MENU DE ACESSIBILIDADE -->
<div id="acessibilidade-menu">
  <h4>Acessibilidade</h4>
  <button onclick="aumentarFonte()">Aumentar Fonte</button>
  <button onclick="diminuirFonte()">Diminuir Fonte</button>
  <button onclick="altoContraste()">Alto Contraste</button>
</div>

<style>
  #acessibilidade-btn {
    position: fixed;
    bottom: 20px;
    left: 20px;
    z-index: 1001;
    cursor: pointer;
  }

  #acessibilidade-btn img {
    width: 55px;
    height: auto;
    transition: transform 0.3s ease;
  }

  #acessibilidade-btn:hover img {
    transform: scale(1.1);
  }

  #acessibilidade-menu {
    position: fixed;
    bottom: 90px;
    left: 20px;
    background: #2c2c2c;
    padding: 1rem;
    border-radius: 10px;
    display: none;
    z-index: 1000;
    box-shadow: 0 0 15px rgba(0,0,0,0.6);
    width: 200px;
  }

  #acessibilidade-menu h4 {
    margin-bottom: 0.5rem;
    color: #fff;
  }

  #acessibilidade-menu button {
    display: block;
    width: 100%;
    margin: 0.3rem 0;
    padding: 0.5rem;
    background-color: #444;
    color: white;
    border: none;
    border-radius: 5px;
    cursor: pointer;
  }

  body.alto-contraste {
    background-color: black !important;
    color: yellow !important;
  }

  body.alto-contraste button {
    background-color: yellow !important;
    color: black !important;
  }
</style>

<script>
  let fonteAtual = 100;

  function toggleAcessibilidade() {
    const menu = document.getElementById("acessibilidade-menu");
    menu.style.display = menu.style.display === "block" ? "none" : "block";
  }

  function aumentarFonte() {
    fonteAtual += 10;
    document.body.style.fontSize = fonteAtual + "%";
  }

  function diminuirFonte() {
    fonteAtual = Math.max(70, fonteAtual - 10);
    document.body.style.fontSize = fonteAtual + "%";
  }

  function altoContraste() {
    document.body.classList.toggle("alto-contraste");
  }
</script>
  <script>
    let sidebar = document.getElementById("sidebar");
    function toggleSidebar() {
      sidebar.classList.toggle("show");
    }

    function toggleTheme() {
      document.body.classList.toggle("light");
      document.getElementById("themeToggle").innerText =
        document.body.classList.contains("light") ? "Tema Escuro" : "Tema Claro";
    }

    function mostrarCompra() {
      document.getElementById("compra").style.display = "block";
    }

    function aplicarDesconto() {
      let cupom = document.getElementById("cupom").value.trim().toUpperCase();
      let info = document.getElementById("descontoInfo");
      if (cupom === "CDL") {
        info.innerText = "Cupom aplicado! Desconto de 20%. Novo valor: R$152,72";
      } else {
        info.innerText = "Cupom inválido.";
      }
    }

    function gerarQR() {
      let container = document.getElementById("qrcode");
      container.innerHTML = "";
      QRCode.toCanvas(document.createElement("canvas"), "Pagamento Think Dog", { width: 150 }, function (err, canvas) {
        container.appendChild(canvas);
      });
      iniciarContagem();
    }

    function iniciarContagem() {
      let tempo = 20 * 60;
      let timer = document.getElementById("timer");
      let intervalo = setInterval(() => {
        let minutos = Math.floor(tempo / 60);
        let segundos = tempo % 60;
        timer.innerText = `QR code expira em ${minutos}:${segundos < 10 ? '0' : ''}${segundos}`;
        tempo--;
        if (tempo < 0) {
          clearInterval(intervalo);
          timer.innerText = "QR code expirado.";
        }
      }, 1000);
    }
  </script>
</body>
</html>
