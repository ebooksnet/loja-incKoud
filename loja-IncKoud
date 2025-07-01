<!DOCTYPE html>
<html lang="pt-br">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>IncKoud | Loja de eBooks</title>
  <style>
    body {
      font-family: 'Segoe UI', sans-serif;
      margin: 0;
      padding: 0;
      background: #f0f4f8;
      color: #333;
    }
    header {
      background: linear-gradient(to right, #1e3c72, #2a5298);
      color: white;
      padding: 20px;
      text-align: center;
      font-size: 2rem;
      font-weight: bold;
    }
    nav {
      display: flex;
      justify-content: center;
      gap: 30px;
      background: #ffffff;
      padding: 15px;
      box-shadow: 0 2px 5px rgba(0,0,0,0.1);
    }
    nav a {
      text-decoration: none;
      color: #1e3c72;
      font-weight: bold;
    }
    .container {
      padding: 30px;
      max-width: 1000px;
      margin: auto;
    }
    .vitrine, .formulario, .compra {
      display: none;
    }
    .ebook-card {
      background: #ffffff;
      border-radius: 15px;
      box-shadow: 0 4px 10px rgba(0,0,0,0.1);
      margin-bottom: 30px;
      padding: 20px;
      display: flex;
      flex-direction: column;
      align-items: center;
      text-align: center;
      transition: transform 0.2s;
    }
    .ebook-card:hover {
      transform: scale(1.02);
    }
    .ebook-card img {
      max-width: 150px;
      border-radius: 10px;
    }
    .btn {
      background: #2a5298;
      color: white;
      padding: 10px 20px;
      margin-top: 10px;
      border: none;
      border-radius: 8px;
      cursor: pointer;
      font-weight: bold;
    }
    .btn:hover {
      background: #1e3c72;
    }
    label, input, textarea {
      display: block;
      width: 100%;
      margin: 10px 0;
    }
  </style>
</head>
<body>
  <header>IncKoud | Sua Loja de eBooks</header>

  <nav>
    <a href="#" onclick="showSection('formulario')">Criar e Enviar eBook</a>
    <a href="#" onclick="showSection('vitrine')">Vitrine</a>
  </nav>

  <div class="container">
    <section id="formulario" class="formulario">
      <h2>Criar e Enviar eBook para Vitrine</h2>
      <form id="ebookForm">
        <label>Título do eBook</label>
        <input type="text" id="titulo" required>
        <label>Imagem da Capa (URL)</label>
        <input type="url" id="imagem" required>
        <label>Descrição</label>
        <textarea id="descricao" required></textarea>
        <label>Preço (R$)</label>
        <input type="number" id="preco" required>
        <button class="btn" type="submit">Enviar para Vitrine</button>
      </form>
    </section>

    <section id="vitrine" class="vitrine">
      <h2>Vitrine de eBooks - IncKoud</h2>
      <div id="vitrineContainer"></div>
    </section>

    <section id="compra" class="compra">
      <h2>Compra por Pix</h2>
      <p>Chave Pix: <strong>inkoud@pagamentos.com</strong></p>
      <p>Após o pagamento, envie o comprovante para nosso WhatsApp: <strong>(99) 99999-9999</strong></p>
    </section>
  </div>

  <script>
    const vitrineContainer = document.getElementById("vitrineContainer");

    document.getElementById("ebookForm").addEventListener("submit", function(event) {
      event.preventDefault();
      const titulo = document.getElementById("titulo").value;
      const imagem = document.getElementById("imagem").value;
      const descricao = document.getElementById("descricao").value;
      const preco = document.getElementById("preco").value;

      const card = document.createElement("div");
      card.className = "ebook-card";
      card.innerHTML = `
        <img src="${imagem}" alt="${titulo}">
        <h3>${titulo}</h3>
        <p>${descricao}</p>
        <p><strong>R$ ${preco}</strong></p>
        <button class="btn" onclick="showSection('compra')">Comprar eBook</button>
      `;

      vitrineContainer.appendChild(card);
      showSection('vitrine');
      document.getElementById("ebookForm").reset();
    });

    function showSection(id) {
      document.querySelectorAll(".formulario, .vitrine, .compra").forEach(sec => sec.style.display = 'none');
      document.getElementById(id).style.display = 'block';
    }

    showSection('formulario');
  </script>
</body>
</html>
