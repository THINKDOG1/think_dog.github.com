<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Think Dog</title>
  <style>
    :root {
      --bg: #f5f5f5;
      --text: #333;
      --card: #fff;
      --accent: #4b3621;
    }
    body.dark {
      --bg: #1e1e1e;
      --text: #f5f5f5;
      --card: #2a2a2a;
    }
    body {
      font-family: 'Segoe UI', sans-serif;
      background-color: var(--bg);
      color: var(--text);
      margin: 0;
      padding: 0;
    }
    header {
      background-color: var(--card);
      padding: 10px 20px;
      display: flex;
      justify-content: space-between;
      align-items: center;
      box-shadow: 0 2px 5px rgba(0,0,0,0.1);
      position: sticky;
      top: 0;
      z-index: 1000;
    }
    .menu-button {
      font-size: 24px;
      background: none;
      border: none;
      cursor: pointer;
      color: var(--text);
    }
    nav {
      display: none;
      flex-direction: column;
      position: absolute;
      top: 60px;
      right: 20px;
      background-color: var(--card);
      box-shadow: 0 2px 5px rgba(0,0,0,0.2);
      border-radius: 8px;
    }
    nav a {
      padding: 10px;
      text-decoration: none;
      color: var(--text);
      font-weight: bold;
    }
    nav a:hover {
      color: var(--accent);
    }
    .store {
      max-width: 960px;
      margin: 0 auto;
      padding: 20px;
    }
    .banner {
      background: linear-gradient(to right, #4b3621, #2f2f2f);
      color: white;
      padding: 30px;
      text-align: center;
      border-radius: 12px;
    }
    .product, .about {
      background: var(--card);
      margin-top: 20px;
      padding: 20px;
      border-radius: 10px;
      box-shadow: 0 2px 5px rgba(0,0,0,0.1);
    }
    .product {
      display: flex;
      flex-direction: column;
      align-items: center;
      gap: 20px;
    }
    .product img {
      width: 300px;
      border-radius: 12px;
      transition: transform 0.3s ease;
    }
    .product img:hover {
      transform: perspective(800px) rotateY(10deg) rotateX(5deg);
    }
    button {
      background-color: var(--accent);
      color: white;
      border: none;
      padding: 10px 16px;
      border-radius: 6px;
      cursor: pointer;
      margin: 5px;
    }
    button:hover {
      background-color: #6f4e37;
    }
    #cart-box, #confirmation, #qrcode-box {
      display: none;
      background-color: var(--card);
      padding: 15px;
      border-radius: 8px;
      margin-top: 20px;
      box-shadow: 0 2px 5px rgba(0,0,0,0.2);
    }
    #extras {
      display: none;
    }
    #discount-message, #confirmation p {
      margin-top: 10px;
      font-weight: bold;
    }
    #countdown {
      color: red;
      font-weight: bold;
    }
  </style>
</head>
<body>
  <header>
    <img src="https://i.imgur.com/p9fncHI.png" alt="Logo Think Dog" style="height: 80px;">
    <button class="menu-button" onclick="toggleMenu()">☰</button>
    <nav id="nav-menu">
      <a href="#">Início</a>
      <a href="#product">Serviços</a>
      <a href="#about">Sobre</a>
      <a href="#suporte">Suporte</a>
      <a href="#" onclick="toggleTheme()">Tema</a>
    </nav>
  </header>

  <div class="store">
    <div class="banner">
      <h1>Think Dog</h1>
      <h2>Traduzimos o que seu cachorro sente, pensa e deseja</h2>
    </div>

    <div class="product" id="product">
      <img src="https://i.imgur.com/iauKggv.jpeg" alt="Serviço Think Dog">
      <div class="product-details">
        <h3>Serviço Think Dog</h3>
        <p>Cada sessão tem o valor de <strong>R$ 239,99</strong>. Envie vídeos ou imagens do seu pet e nossa equipe de especialistas traduzirá o que ele quer comunicar!</p>
        <button onclick="showExtras()">Quero contratar</button>
      </div>

      <div id="extras">
        <label for="discount">Código de Desconto:</label>
        <input type="text" id="discount" placeholder="Digite seu código">
        <button onclick="applyDiscount()">Aplicar código</button>
        <div id="discount-message"></div>
        <button onclick="addToCart()">Adicionar ao carrinho</button>
        <button onclick="buyNow()">Comprar agora</button>
        <div id="cart-box">
          <p>Itens no carrinho: <span id="cart-count">0</span></p>
          <p>Total: R$ <span id="cart-total">0.00</span></p>
          <button onclick="finalizePurchase()">Finalizar compra</button>
        </div>
        <div id="confirmation"></div>
        <div id="qrcode-box">
          <p>QR Code de pagamento (expira em <span id="countdown">20:00</span>):</p>
          <img src="https://api.qrserver.com/v1/create-qr-code/?data=PagamentoThinkDog&size=200x200" alt="QR Code" style="width: 120px; height: 120px;">
      </div>

    <section class="about" id="about">
      <h3>Sobre a Think Dog</h3>
      <p>A <strong>Think Dog</strong> é uma empresa apaixonada por tecnologia e pets. Nosso serviço principal oferece tradução comportamental dos sentimentos e pensamentos do seu cachorro por meio de especialistas qualificados.</p>
      <h4>Apoie a Adoção de Cães</h4>
      <p>Parte da renda das vendas é destinada a ONGs de resgate. Incentivamos a adoção responsável.</p>
      <h4>Parceria com a Fundação CDL</h4>
      <p>Com apoio da <strong>Fundação CDL</strong>, promovemos bem-estar animal com tecnologia e empatia.</p>
    </section>

    <section class="about" id="suporte">
      <h3>Suporte</h3>
      <p>Em caso de dúvidas ou problemas com sua compra, entre em contato com nosso suporte via WhatsApp:</p>
      <p><a href="https://chat.whatsapp.com/EHBXUktjBP78tAGb1OpL4s" target="_blank">Entrar no grupo de suporte</a></p>
    </section>
  </div>

  <script>
    let cartCount = 0;
    let cartTotal = 0;
    let discountApplied = false;
    let timerInterval;

    function toggleTheme() {
      document.body.classList.toggle('dark');
    }
    function toggleMenu() {
      const nav = document.getElementById('nav-menu');
      nav.style.display = nav.style.display === 'flex' ? 'none' : 'flex';
    }
    function showExtras() {
      document.getElementById('extras').style.display = 'block';
    }
    function applyDiscount() {
      const code = document.getElementById('discount').value.trim().toUpperCase();
      const message = document.getElementById('discount-message');
      if (code === 'CDL') {
        discountApplied = true;
        message.innerText = "Desconto de 50% aplicado com sucesso!";
        message.style.color = "green";
      } else {
        discountApplied = false;
        message.innerText = "Código inválido ou expirado.";
        message.style.color = "red";
      }
    }
    function addToCart() {
      let price = 239.99;
      if (discountApplied) price *= 0.5;
      cartCount++;
      cartTotal += price;
      document.getElementById('cart-count').innerText = cartCount;
      document.getElementById('cart-total').innerText = cartTotal.toFixed(2);
      document.getElementById('cart-box').style.display = 'block';
    }
    function buyNow() {
      addToCart();
    }
    function finalizePurchase() {
      document.getElementById('confirmation').innerHTML = '<p>Compra finalizada com sucesso! Seu QR Code de pagamento está abaixo:</p>';
      document.getElementById('confirmation').style.display = 'block';
      document.getElementById('qrcode-box').style.display = 'block';
      startCountdown();
    }
    function startCountdown() {
      let duration = 20 * 60;
      const countdownEl = document.getElementById('countdown');
      clearInterval(timerInterval);
      timerInterval = setInterval(() => {
        let minutes = Math.floor(duration / 60);
        let seconds = duration % 60;
        countdownEl.textContent = `${minutes}:${seconds.toString().padStart(2, '0')}`;
        if (--duration < 0) {
          clearInterval(timerInterval);
          countdownEl.textContent = 'Expirado';
        }
      }, 1000);
    }
  </script>
</body>
</html>



