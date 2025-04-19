<!DOCTYPE html>
<html lang="pt-br">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Manos Barber's</title>
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: 'Segoe UI', sans-serif;
    }

    body {
      background: linear-gradient(to bottom, #000000, #111111);
      color: white;
    }
/* Tela de carregamento futurista */
#welcome {
  position: fixed;
  width: 100%;
  height: 100vh;
  background: linear-gradient(145deg, #2e2e2e, #1c1c1c);
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  z-index: 9999;
  overflow: hidden;
  animation: fadeIn 1s ease-in-out;
}

.loader-circle {
  border: 5px solid rgba(255, 255, 255, 0.2);
  border-top: 5px solid #ff0000;
  border-radius: 50%;
  width: 60px;
  height: 60px;
  animation: spin 1s linear infinite;
  margin-bottom: 30px;
}

#typewriter {
  font-size: 2.5rem;
  color: #fff;
  font-family: 'Courier New', monospace;
  white-space: nowrap;
  border-right: 2px solid #fff;
  overflow: hidden;
  width: 0;
  animation: typing 2s steps(20) 0.5s forwards, blink 0.7s step-end infinite;
  text-shadow: 0 0 10px red;
}

.subtext {
  font-size: 1rem;
  color: #ccc;
  margin-top: 10px;
  font-style: italic;
  opacity: 0;
  animation: fadeInSub 2s ease-in-out 3s forwards;
}

/* Animações */
@keyframes fadeIn {
  from { opacity: 0; }
  to { opacity: 1; }
}

@keyframes typing {
  from { width: 0 }
  to { width: 15ch }
}

@keyframes blink {
  0%, 100% { border-color: transparent; }
  50% { border-color: #fff; }
}

@keyframes fadeInSub {
  from { opacity: 0; transform: translateY(10px); }
  to { opacity: 1; transform: translateY(0); }
}

@keyframes spin {
  0% { transform: rotate(0deg); }
  100% { transform: rotate(360deg); }
}
   

    /* Nome "Manos Barber's" */
     }

    .quote {
      text-align: center;
      margin: 10px;
      font-style: italic;
      color: #ccc;
    }

    .menu-icon {
      position: absolute;
      top: 20px;
      right: 20px;
      font-size: 2rem;
      cursor: pointer;
      z-index: 10000;
    }

    .sidebar {
      position: fixed;
      top: 0;
      right: -250px;
      width: 250px;
      height: 100%;
      background: #1a1a1a;
      padding: 30px;
      transition: right 0.3s ease;
      z-index: 9998;
      box-shadow: -2px 0 10px rgba(255, 0, 0, 0.3);
    }

    .sidebar.active {
      right: 0;
    }

    .sidebar a {
      display: block;
      margin: 20px 0;
      color: white;
      text-decoration: none;
      font-size: 1.2rem;
    }

    section {
      padding: 40px 20px;
    }

    h2 {
      font-size: 2rem;
      margin-bottom: 20px;
      border-left: 5px solid red;
      padding-left: 10px;
    }

    .service {
      margin-bottom: 20px;
      padding: 15px;
      border-radius: 10px;
      background: linear-gradient(to right, #222, #333);
      box-shadow: 0 0 10px rgba(255, 0, 0, 0.2);
    }

    .service h3 {
      font-size: 1.5rem;
      margin-bottom: 5px;
      color: #f0f0f0;
    }

    .service p {
      color: #aaa;
    }

    .whatsapp-btn {
  position: fixed;
  bottom: 30px;
  right: 30px;
  width: 60px;
  height: 60px;
  background: #25D366;
  border-radius: 50%;
  box-shadow: 0 0 15px #25D366;
  display: flex;
  align-items: center;
  justify-content: center;
  transition: transform 0.3s ease, box-shadow 0.3s ease;
  z-index: 9999;
}

.whatsapp-btn img {
  width: 30px;
  height: 30px;
}

.whatsapp-btn:hover {
  transform: scale(1.1);
  box-shadow: 0 0 20px #25D366, 0 0 30px #25D366;
}
    /* Imagens */
    .img-area {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 15px;
    }

    .img-area img {
      max-width: 200px;
      border-radius: 15px;
      box-shadow: 0 0 10px red;
    }

    /* Nova foto do cabeçalho */
    header img {
      width: 100%;
      height: auto;
      border-radius: 10px;
      margin-top: 20px;
      transition: transform 0.3s ease;
    }

    /* Efeito 3D na foto ao passar o mouse */
    header img:hover {
      transform: scale(1.1) rotate(5deg);
    }
  
  }
}
  </style>
</head>
<body>

  <div id="welcome">
  <div class="loader-circle"></div>
  <h1 id="typewriter"></h1>
  <p class="subtext">Afiando as lâminas...</p>
</div>
  


<!-- Botão Menu Hambúrguer -->
<div class="menu-toggle" id="menu-toggle">
  <span class="bar"></span>
  <span class="bar"></span>
  <span class="bar"></span>
</div>

<!-- Menu Lateral Direito -->
<nav id="menu" class="menu-hidden"></nav>

  
    <style>
    @import url('https://fonts.googleapis.com/css2?family=Lemon+Milk&display=swap');

    .title {
        font-family: 'Lemon Milk', sans-serif;
        font-size: 4rem;
        color: black; /* Cor preta */
        text-transform: uppercase;
        letter-spacing: 5px;
        text-shadow: 3px 3px 10px rgba(0, 0, 0, 0.5), 0 0 20px red;
        text-align: center;
        margin: 0;
    }

    .quote {
        font-family: 'Segoe UI', sans-serif;
        font-size: 1.5rem;
        font-style: italic;
        color: #ccc;
        margin-top: 10px;
        text-shadow: 1px 1px 5px rgba(0, 0, 0, 0.5);
        text-align: center;
    }
    .agendar-btn {
  display: inline-block;
  margin-top: 10px;
  padding: 8px 16px;
  background: linear-gradient(45deg, #ff0000, #0000ff);
  color: white;
  border: none;
  border-radius: 8px;
  text-decoration: none;
  font-weight: bold;
  transition: transform 0.3s, box-shadow 0.3s;
  box-shadow: 0 0 10px rgba(255, 0, 0, 0.5);
}

.agendar-btn:hover {
  transform: scale(1.05);
  box-shadow: 0 0 15px rgba(0, 0, 255, 0.5);
}
</style>

<h1 class="title"></h1>
<p class="quote"></p></header>
  <div style="text-align: center; padding: 10px;">
  <img src="https://i.imgur.com/eAqHQxs.png" alt="Logo Manos Barber's" style="max-width: 200px; height: auto;">
    </div
<style>
    
</style>

<style>
    /* Fonte Lemon Milk */
    @import url('https://fonts.googleapis.com/css2?family=Lemon+Milk&display=swap');

    /* Estilo para o título */
    .title {
        font-family: 'Lemon Milk', sans-serif;
        font-size: 4rem;
        color: #f5f5f5;
        text-transform: uppercase;
        letter-spacing: 5px;
        text-shadow: 3px 3px 10px rgba(0, 0, 0, 0.5), 0 0 20px red;
        display: flex;
        justify-content: center;
        align-items: center;
        margin: 0;
    }

    .letter {
        display: inline-block;
        transition: transform 0.3s ease;
    }

  
    /* Efeito ao passar o mouse */
    .letter:hover {
        transform: rotate(0deg) scale(1.2);
    }

    /* Estilo para a citação */
    .quote {
        font-family: 'Segoe UI', sans-serif;
        font-size: 1.5rem;
        font-style: italic;
        color: #ccc;
        margin-top: 10px;
        text-shadow: 1px 1px 5px rgba(0, 0, 0, 0.5);
    }
</style>

  <section id="conheca">
  <h2 style="background: linear-gradient(135deg, #ff0000, #0000ff, #000000); -webkit-background-clip: text; color: transparent;">CONHEÇA A BARBEARIA</h2>
  <p style="font-size: 1.2rem; color: white;">Localizada em Vista Alegre, Belo Horizonte, a <span style="font-weight: bold; color: #ff4c4c;">Manos Barber's</span> é uma barbearia que segue um estilo clássico e acolhedor. Com mais de 10 anos no ramo, a barbearia é comandada por Renato, que traz experiência e excelência em cada corte.</p>
  <p style="font-size: 1.2rem; color: white;">Na <span style="font-weight: bold; color: #ff4c4c;">Manos Barber's</span>, o cliente é tratado com respeito e carinho, sempre buscando o melhor estilo e atendimento personalizado. Nosso objetivo é proporcionar a melhor experiência em cortes de cabelo, barba e outros serviços, mantendo um ambiente confortável e de confiança.</p>
  <p style="font-size: 1.2rem; color: white;">Venha conhecer nosso trabalho e se sentir em casa. Garantimos que você sairá com um <span style="font-weight: bold; color: #ff4c4c;">visual impecável!</span></p>
</section>
 <style>
  .image-container {
    width: 100%;
    max-width: 500px; /* Limita o tamanho da imagem */
    margin: 20px auto;
    padding: 10px;
    border-radius: 15px;
    background-color: #222;
    box-shadow: 0 0 15px rgba(255, 0, 0, 0.3);
    overflow: hidden;
    perspective: 1000px; /* Adiciona a perspectiva para o efeito 3D */
  }

  .image-container img {
    width: 100%;
    height: auto;
    border-radius: 10px;
    transition: transform 0.3s ease;
    transform-style: preserve-3d; /* Habilita o efeito 3D */
  }

  /* Efeito 3D suave no hover */
  .image-container:hover img {
    transform: rotateY(5deg) rotateX(5deg); /* Menos rotação para efeito 3D mais sutil */
  }

  /* Efeito 3D suave no clique */
  .image-container:active img {
    transform: rotateY(10deg) rotateX(10deg); /* Menos rotação ao clicar */
  }
</style>

  <style>
  .service {
    opacity: 0;
    transform: translateY(40px);
    transition: opacity 0.8s ease-out, transform 0.8s ease-out;
  }

  .service.visible {
    opacity: 1;
    transform: translateY(0);
  }
</style>
  
<!-- Box com imagem -->
<div class="image-container">
  <img src="https://i.imgur.com/5WJtGzt.jpeg" alt="Imagem 3D">
</div>
  <style>
  .agendar-btn {
    display: inline-block;
    margin-top: 10px;
    padding: 10px 20px;
    background: #111;
    color: #fff;
    font-weight: bold;
    border-radius: 8px;
    text-decoration: none;
    box-shadow: 0 4px 10px rgba(255, 0, 0, 0.2);
    transition: all 0.3s ease;
    border: 1px solid #333;
  }

  .agendar-btn:hover {
    background: #ff0000;
    color: #fff;
    transform: scale(1.05);
    box-shadow: 0 6px 15px rgba(255, 0, 0, 0.4);
  }

  .agendar-btn img {
    width: 18px;
    vertical-align: middle;
    margin-right: 8px;
  }
</style>

<section id="servicos">
  <h2 style="background: linear-gradient(135deg, #b80000, #222); -webkit-background-clip: text; color: transparent;">NOSSOS SERVIÇOS</h2>

  <div class="service">
    <h3>Corte de cabelo - R$ ???</h3>
    <p>Corte de todos os estilos</p>
    <a href="https://wa.me/553192935872?text=Olá! Gostaria de agendar um corte de cabelo." target="_blank" class="agendar-btn">
      <img src="https://cdn-icons-png.flaticon.com/512/124/124034.png" alt="WhatsApp"> Agendar Corte
    </a>
  </div>

  <div class="service">
    <h3>Barba com toalha quente - R$ ???</h3>
    <p>Procedimento com massageador</p>
    <a href="https://wa.me/553192935872?text=Olá! Gostaria de agendar uma barba com toalha quente." target="_blank" class="agendar-btn">
      <img src="https://cdn-icons-png.flaticon.com/512/124/124034.png" alt="WhatsApp"> Agendar Barba
    </a>
  </div>

  <div class="service">
    <h3>Corte e Barba - R$ ???</h3>
    <p>Combo promocional</p>
    <a href="https://wa.me/553192935872?text=Olá! Gostaria de agendar um combo de corte e barba." target="_blank" class="agendar-btn">
      <img src="https://cdn-icons-png.flaticon.com/512/124/124034.png" alt="WhatsApp"> Agendar Combo
    </a>
  </div>

  <div class="service">
    <h3>Pezinho - R$ ???</h3>
    <p>Acabamento</p>
    <a href="https://wa.me/553192935872?text=Olá! Gostaria de agendar um pezinho." target="_blank" class="agendar-btn">
      <img src="https://cdn-icons-png.flaticon.com/512/124/124034.png" alt="WhatsApp"> Agendar Pezinho
    </a>
  </div>

  <div class="service">
    <h3>Barboterapia - R$ ???</h3>
    <p>Limpeza de pele, esfoliação e massagem</p>
    <a href="https://wa.me/553192935872?text=Olá! Gostaria de agendar uma barboterapia." target="_blank" class="agendar-btn">
      <img src="https://cdn-icons-png.flaticon.com/512/124/124034.png" alt="WhatsApp"> Agendar Barboterapia
    </a>
  </div>

  <div class="service">
    <h3>Selagem cabelo curto - R$ ???</h3>
    <p>Recuperação capilar</p>
    <a href="https://wa.me/553192935872?text=Olá! Gostaria de agendar uma selagem para cabelo curto." target="_blank" class="agendar-btn">
      <img src="https://cdn-icons-png.flaticon.com/512/124/124034.png" alt="WhatsApp"> Agendar Selagem
    </a>
  </div>

  <div class="service">
    <h3>Reconstrução cabelo curto - R$ ???</h3>
    <p>Hidratação intensiva</p>
    <a href="https://wa.me/553192935872?text=Olá! Gostaria de agendar uma reconstrução para cabelo curto." target="_blank" class="agendar-btn">
      <img src="https://cdn-icons-png.flaticon.com/512/124/124034.png" alt="WhatsApp"> Agendar Reconstrução
    </a>
  </div>

  <div class="service">
    <h3>Tintura cabelo curto - R$ ???</h3>
    <p>Com produtos selecionados</p>
    <a href="https://wa.me/553192935872?text=Olá! Gostaria de agendar uma tintura para cabelo curto." target="_blank" class="agendar-btn">
      <img src="https://cdn-icons-png.flaticon.com/512/124/124034.png" alt="WhatsApp"> Agendar Tintura
    </a>
  </div>

  <div class="service">
    <h3>Tintura para barba - R$ ???</h3>
    <p>Com produtos selecionados</p>
    <a href="https://wa.me/553192935872?text=Olá! Gostaria de agendar uma tintura para barba." target="_blank" class="agendar-btn">
      <img src="https://cdn-icons-png.flaticon.com/512/124/124034.png" alt="WhatsApp"> Agendar Tintura Barba
    </a>
  </div>

  <div class="service">
    <h3>Reflexo - ???</h3>
    <p>A definir</p>
    <a href="https://wa.me/553192935872?text=Olá! Gostaria de saber mais sobre o serviço de reflexo." target="_blank" class="agendar-btn">
      <img src="https://cdn-icons-png.flaticon.com/512/124/124034.png" alt="WhatsApp"> Agendar Reflexo
    </a>
  </div>
</section>

  <a href="https://wa.me/553192935872?text=Ol%C3%A1%2C+gostaria+de+agendar+um+hor%C3%A1rio+na+Manos+Barber%27s." target="_blank" class="whatsapp-btn">
  <img src="https://cdn.jsdelivr.net/gh/edent/SuperTinyIcons/images/svg/whatsapp.svg" alt="WhatsApp" />
</a>
  
<style>
  .rating {
    display: flex;
    gap: 5px;
    font-size: 2rem;
    color: #f4c542;
  }
  .rating input {
    display: none;
  }
  .rating label {
    cursor: pointer;
  }
  .rating input:checked ~ label {
    color: #f4c542;
  }
</style>
  <section id="localizacao" style="
  max-width: 600px;
  margin: 40px auto;
  padding: 25px;
  background: #ffffff10;
  backdrop-filter: blur(6px);
  border-radius: 16px;
  border: 1px solid rgba(255, 255, 255, 0.1);
  box-shadow: 0 0 15px rgba(0, 0, 0, 0.3);
  text-align: center;
  color: #fff;
">
  <section id="localizacao">
  <h2>Onde Estamos</h2>
  <p><strong>Barbearia Manos</strong></p>
  <p>📍 Avenida Padre José Maurício, 1239 – Vista Alegre, Belo Horizonte – MG, CEP: 30514-000</p>
  <p>📞 55 31 3657-5047</p>
  <a href="https://www.google.com/maps?q=Barbearia+Manos,+Avenida+Padre+José+Maurício,+1239,+Vista+Alegre,+Belo+Horizonte,+MG" target="_blank">
    <img src="https://i.imgur.com/QPLgNgp.jpeg" alt="Localização da Barbearia" style="width: 100%; max-width: 500px; border-radius: 10px;">
  </a>
</section>
    <!-- Carrossel de Cortes de Cabelo -->
<div class="carrossel-container">
  <div class="carrossel">
    <div class="item">
      <img src="https://i.imgur.com/WRijyUG.jpeg" alt="Corte Americano">
      <div class="nome-corte">Americano</div>
    </div>
    <div class="item">
      <img src="https://i.imgur.com/mL32ei7.jpeg" alt="Corte Mid Fade">
      <div class="nome-corte">Mid Fade</div>
    </div>
    <div class="item">
      <img src="https://i.imgur.com/l6K5cFn.jpeg" alt="Corte Mullet">
      <div class="nome-corte">Mullet</div>
    </div>
  </div>
  <!-- Botões de navegação -->
  <span class="prev" onclick="moveToPrevious()">&#10094;</span>
  <span class="next" onclick="moveToNext()">&#10095;</span>
</div>

<style>
  * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }

  body {
    font-family: 'Lemon Milk', sans-serif;
    background-color: #121212;
    color: #fff;
    margin: 0;
  }

  .carrossel-container {
    position: relative;
    width: 90%;
    max-width: 1000px;
    margin: 50px auto;
    overflow: hidden;
    border-radius: 15px;
    box-shadow: 0 0 30px rgba(0, 0, 0, 0.5);
    border: 2px solid rgba(255, 255, 255, 0.2);
  }

  .carrossel {
    display: flex;
    transition: transform 0.7s ease-in-out;
  }

  .item {
    position: relative;
    flex: 0 0 100%;
    overflow: hidden;
    display: flex;
    justify-content: center;
    align-items: center;
  }

  .item img {
    width: 100%;
    height: auto;
    object-fit: cover;
    border-radius: 15px;
  }

  .nome-corte {
    position: absolute;
    top: 10%;
    left: 50%;
    transform: translateX(-50%);
    font-size: 28px;
    color: white;
    text-shadow: 2px 2px 10px rgba(0, 0, 0, 0.8);
    font-weight: bold;
    letter-spacing: 2px;
    background-color: rgba(0, 0, 0, 0.5);
    padding: 10px 20px;
    border-radius: 8px;
  }

  /* Botões de navegação */
  .prev, .next {
    position: absolute;
    top: 50%;
    transform: translateY(-50%);
    background-color: rgba(0, 0, 0, 0.5);
    color: white;
    font-size: 30px;
    padding: 15px;
    cursor: pointer;
    border: none;
    border-radius: 50%;
    z-index: 1000;
    transition: background-color 0.3s ease;
  }

  .prev:hover, .next:hover {
    background-color: rgba(255, 255, 255, 0.3);
  }

  .prev {
    left: 20px;
  }

  .next {
    right: 20px;
  }

  /* Responsividade */
  @media (max-width: 768px) {
    .nome-corte {
      font-size: 20px;
    }

    .prev, .next {
      padding: 12px;
      font-size: 24px;
    }
  }

  /* Estilos de transição */
  .carrossel {
    transition: transform 0.7s cubic-bezier(0.25, 0.8, 0.25, 1);
  }
</style>

<script>
  let currentIndex = 0;
  const items = document.querySelectorAll('.item');
  const totalItems = items.length;

  // Função para mover para o próximo item
  function moveToNext() {
    if (currentIndex < totalItems - 1) {
      currentIndex++;
    } else {
      currentIndex = 0; // Volta para o primeiro
    }
    updateCarousel();
  }

  // Função para mover para o item anterior
  function moveToPrevious() {
    if (currentIndex > 0) {
      currentIndex--;
    } else {
      currentIndex = totalItems - 1; // Vai para o último
    }
    updateCarousel();
  }

  // Função para atualizar o carrossel
  function updateCarousel() {
    const newTransformValue = -currentIndex * 100;
    document.querySelector('.carrossel').style.transform = `translateX(${newTransformValue}%)`;
  }
</script>
  <footer>
  <p>&copy; 2025 <span class="footer-brand">Manos Barber's</span>. Todos os direitos reservados.</p>
</footer>

<style>
  <script>
  const toggle = document.getElementById("menu-toggle");
  const menu = document.getElementById("menu");

  toggle.addEventListener("click", () => {
    toggle.classList.toggle("active");
    menu.classList.toggle("menu-active");
  });

  // Botão para voltar ao topo
  const topButton = document.getElementById("topButton");

  window.addEventListener("scroll", () => {
    if (window.scrollY > 200) {
      topButton.style.display = "block";
    } else {
      topButton.style.display = "none";
    }
  });

  topButton.addEventListener("click", () => {
    window.scrollTo({ top: 0, behavior: 'smooth' });
  });
</script>
    footer {
    text-align: center;
    padding: 20px;
    background: linear-gradient(135deg, #1a1a1a, #333333);
    color: white;
    box-shadow: 0px -4px 10px rgba(0, 0, 0, 0.3);
    position: fixed;
    width: 100%;
    bottom: 0;
  }

  .footer-brand {
    font-weight: bold;
    color: #f44336; /* cor vermelha para destaque */
    text-transform: uppercase;
  }

  footer p {
    font-size: 1rem;
    letter-spacing: 1px;
  }
</style>
   
   <script>
    
  function revealServices() {
    const services = document.querySelectorAll('.service');
    const triggerBottom = window.innerHeight * 0.85;

    services.forEach(service => {
      const serviceTop = service.getBoundingClientRect().top;

      if (serviceTop < triggerBottom) {
        service.classList.add('visible');
      }
    });
  }

  window.addEventListener('scroll', revealServices);
  window.addEventListener('load', revealServices);
</script>
    
   <script>
  const menuToggle = document.getElementById('menu-toggle');
const menu = document.getElementById('menu');

menuToggle.addEventListener('click', () => {
  menuToggle.classList.toggle('active');
  menu.classList.toggle('hidden');
});
  
  const texto = "Manos Barber";
  let i = 0;

  function typeEffect() {
    const el = document.getElementById("typewriter");
    if (i < texto.length) {
      el.innerHTML += texto.charAt(i);
      i++;
      setTimeout(typeEffect, 100);
    }
      window.onload = function() {
  window.scrollTo(0, 0); // Rola para o topo
};
  }
  
 

  window.onload = () => {
    typeEffect();
    // Remove a tela após 4s
    setTimeout(() => {
      const welcome = document.getElementById("welcome");
      welcome.style.transition = "opacity 1s ease";
      welcome.style.opacity = "0";
      setTimeout(() => welcome.remove(), 1000);
    }, 4000);
  };
function enterSite() {
      const welcome = document.getElementById('welcome');
      welcome.style.opacity = '0';
      setTimeout(() => {
        welcome.style.display = 'none';
      }, 1000); // Aguarda a animação antes de esconder
    }

    function toggleMenu() {
      const sidebar = document.getElementById('sidebar');
      sidebar.classList.toggle('active');
    }
    
  </script>
</body>
</html>
