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
    <img src="https://i.imgur.com/rG5a0Sa.png" alt="Think Dog Logo" class="logo" />
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
        <p>Transformamos a comunicação entre humanos e cachorros. Com apoio da Fundação CDL, oferecemos sessões onde nossos profissionais traduzem os pensamentos dos cães para seus donos. Cada sessão custa R$239,99.</p>
        <div class="quote">"Seu doguinho tem muito a dizer. Nós traduzimos para você entender."</div>
      </div>
    </section>

    <section id="servicos" class="services">
      <h3>Serviço Think Dog</h3>
      <p>• Sessões com tradutores especializados em comportamento canino.<br>• Cada sessão: <strong>R$239,99</strong></p>
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
      <p>"Nunca entendi tanto meu doguinho, obrigado Think Dog!"</p>
      <p>"Achei que era brincadeira, mas fiquei emocionado com a sessão."</p>
    </section>

    <section class="avaliar">
      <h3>Avalie nosso site</h3>
      <input type="text" placeholder="Digite seu feedback..." />
      <button>Enviar</button>
    </section>
  </main>

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
        info.innerText = "Cupom aplicado! Desconto de 50%. Novo valor: R$119,99";
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


