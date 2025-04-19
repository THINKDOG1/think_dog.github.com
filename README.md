<!DOCTYPE html>
<html lang="pt-br">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Manual do Alpha Moderno</title>
  <link href="https://fonts.googleapis.com/css2?family=Anton&family=Montserrat:wght@400;700&display=swap" rel="stylesheet">
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      scroll-behavior: smooth;
      font-family: 'Montserrat', sans-serif;
    }

    body {
      background-color: #000;
      color: white;
    }

    /* TOPO */
    .top-bar {
      background: linear-gradient(to right, #3d0066, #6e00b3);
      color: white;
      text-align: center;
      padding: 10px;
      font-weight: bold;
      font-size: 14px;
    }

    .hero {
      background: linear-gradient(135deg, #000, #111, #222);
      text-align: center;
      padding: 100px 20px;
    }

    .hero h1 {
      font-family: 'Anton', sans-serif;
      font-size: 3.5rem;
      color: #b45eff;
      margin-bottom: 20px;
      letter-spacing: 2px;
    }

    .hero .frase {
      font-size: 1.2rem;
      color: #ccc;
      margin-bottom: 30px;
    }

    .btn, .btn-destaque {
      background-color: #b45eff;
      color: #000;
      padding: 15px 30px;
      border: none;
      border-radius: 30px;
      font-weight: bold;
      cursor: pointer;
      transition: all 0.3s ease;
      text-decoration: none;
    }

    .btn:hover, .btn-destaque:hover {
      transform: scale(1.05);
      box-shadow: 0 0 15px #b45eff;
    }

    .btn-destaque {
      font-size: 1.2rem;
      padding: 20px 40px;
      border-radius: 40px;
      display: inline-block;
    }

    section {
      padding: 60px 20px;
      text-align: center;
    }

    h2 {
      color: #b45eff;
      font-size: 2.2rem;
      margin-bottom: 20px;
    }

    .modulos ul {
      list-style: none;
      max-width: 600px;
      margin: 0 auto;
    }

    .modulos li {
      background-color: #222;
      margin: 10px 0;
      padding: 15px;
      border-left: 5px solid #b45eff;
      border-radius: 10px;
    }

    .card {
      background: #1a1a1a;
      padding: 20px;
      margin: 15px auto;
      max-width: 600px;
      border-radius: 15px;
      box-shadow: 0 0 10px #000;
    }

    .card p {
      font-style: italic;
      margin-bottom: 10px;
    }

    .card span {
      color: #b45eff;
      font-weight: bold;
    }

    .cta {
      background: #000;
      padding: 80px 20px;
    }

    .imagem-curso {
      margin-top: 30px;
    }

    .imagem-curso img {
      max-width: 90%;
      height: auto;
      border-radius: 15px;
      transition: transform 0.3s ease, box-shadow 0.3s ease;
    }

    .imagem-curso img:hover {
      transform: scale(1.02);
      box-shadow: 0 0 20px #b45eff;
    }

    .whatsapp-btn {
      position: fixed;
      bottom: 20px;
      right: 20px;
      background: #25D366;
      color: #fff;
      padding: 15px 20px;
      border-radius: 50px;
      text-decoration: none;
      font-weight: bold;
      box-shadow: 0 0 10px #25D366;
    }

    footer {
      background: #0d0d0d;
      padding: 30px;
      text-align: center;
      color: #777;
      font-size: 0.9rem;
    }

    /* EFEITO ANIMAÇÃO */
    .fade-up {
      opacity: 0;
      transform: translateY(40px);
      transition: all 0.8s ease;
    }

    .fade-up.visible {
      opacity: 1;
      transform: translateY(0);
    }

    .box {
      background-color: #0a0a0a;
      border: 1px solid #8000ff;
      border-radius: 12px;
      padding: 25px 15px;
      margin: 25px auto;
      width: 90%;
      max-width: 600px;
      text-align: center;
      box-shadow: 0 0 15px #8000ff50;
      opacity: 0;
      transform: translateY(40px);
      animation: fadeUp 1s ease forwards;
    }

    .box-icon {
      font-size: 48px;
      margin-bottom: 15px;
    }

    .box p {
      font-size: 18px;
      font-weight: bold;
      opacity: 0;
      transform: translateX(-50px);
      animation: fadeText 1s ease forwards;
      animation-delay: 0.4s;
    }

    @keyframes fadeUp {
      to {
        opacity: 1;
        transform: translateY(0);
      }
    }

    @keyframes fadeText {
      to {
        opacity: 1;
        transform: translateX(0);
      }
    }
  </style>
</head>
<body>
  <div class="top-bar">5 VIDEO AULAS EXCLUSIVAS HOJE</div>

  <section class="hero fade-up">
    <h1>Manual do Alpha Moderno</h1>
    <p class="frase">Torne-se o homem que impõe respeito em silêncio e atrai olhares sem esforço.</p>
    <a href="#sobre" class="btn">Descubra Agora</a>
  </section>

  <section id="sobre" class="sobre fade-up">
    <h2>O que é o Manual do Alpha Moderno?</h2>
    <p>Um curso completo voltado para iniciantes no desenvolvimento pessoal, físico e mental. Transforme sua vida com técnicas práticas e estratégias para se tornar um homem mais confiante, influente e naturalmente atraente.</p>
    <div class="imagem-curso fade-up">
      <a href="https://bit.ly/Mentor_alpha2" target="_blank">
        <img src="https://i.imgur.com/MkvuXvw.png" alt="Manual do Alpha Moderno" />
      </a>
    </div>
  </section>

  <section class="modulos fade-up">
    <h2>O que você vai aprender:</h2>
    <ul>
      <li class="fade-up">Autoconfiança e linguagem corporal</li>
      <li class="fade-up">Estilo e aparência pessoal</li>
      <li class="fade-up">Controle emocional e mentalidade</li>
      <li class="fade-up">Como atrair mulheres naturalmente</li>
      <li class="fade-up">Liderança, disciplina e hábitos</li>
    </ul>
  </section>

  <section class="depoimentos fade-up">
    <h2>Transformações reais</h2>
    <div class="card fade-up">
      <p>"Depois que apliquei o que aprendi aqui, minha postura mudou totalmente. As pessoas me tratam diferente."</p>
      <span>— João M.</span>
    </div>
    <div class="card fade-up">
      <p>"Nunca imaginei que com simples mudanças de atitude eu chamaria tanta atenção sem dizer nada."</p>
      <span>— Rafael D.</span>
    </div>
  </section>

  <section class="cta fade-up">
    <h2>Pronto para sua transformação?</h2>
    <a href="https://bit.ly/Mentor_alpha2" class="btn-destaque">Acessar Agora (R$ ???)</a>
  </section>

  <div class="box"><div class="box-icon">✖️</div><p>Não sabe como ter assuntos interessantes com uma mulher.</p></div>
  <div class="box"><div class="box-icon">📴</div><p>Só fica no vácuo e não consegue entender o real motivo.</p></div>
  <div class="box"><div class="box-icon">💬❌</div><p>Não consegue despertar desejo e muito menos o interesse sexual em uma mulher</p></div>
  <div class="box"><div class="box-icon">😬</div><p>Tem falta de autoestima e confiança.</p></div>
  <div class="box"><div class="box-icon">🙈</div><p>Tem medo de ser julgado e ridicularizado pelos seus amigos e pela sociedade.</p></div>
  <div class="box"><div class="box-icon">💔</div><p>Tem a vida sexual limitada e isso está acabando com a sua saúde mental e emocional.</p></div>

  <a class="whatsapp-btn" href="https://wa.me/5587982022078" target="_blank">Fale com a gente</a>

  <footer class="fade-up">
    <p>By Apoenno Rodrigues</p>
    <p>© 2025 Manual do Alpha Moderno. Todos os direitos reservados.</p>
  </footer>

  <script>
    const elements = document.querySelectorAll('.fade-up');

    function showOnScroll() {
      const trigger = window.innerHeight * 0.9;

      elements.forEach(el => {
        const top = el.getBoundingClientRect().top;
        if (top < trigger) {
          el.classList.add('visible');
        }
      });
    }

    window.addEventListener('scroll', showOnScroll);
    window.addEventListener('load', showOnScroll);
  </script>
</body>
</html>
