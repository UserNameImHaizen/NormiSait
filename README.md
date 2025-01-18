<!DOCTYPE html>
<html lang="ru">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Онлайн Магазин</title>
  <style>
    body {
      margin: 0;
      font-family: Arial, sans-serif;
      background-color: #000;
      color: #fff;
    }
    header {
      background-color: #111;
      padding: 20px;
      text-align: center;
    }
    nav {
      display: flex;
      justify-content: center;
      margin: 20px 0;
    }
    nav a {
      color: #fff;
      text-decoration: none;
      margin: 0 15px;
      padding: 10px 20px;
      border: 1px solid #fff;
      border-radius: 5px;
      transition: background-color 0.3s;
    }
    nav a:hover {
      background-color: #333;
    }
    .section {
      display: none;
      padding: 20px;
      text-align: center;
    }
    .section.active {
      display: block;
    }
    .product {
      margin: 20px auto;
      padding: 20px;
      background-color: #222;
      border: 1px solid #444;
      border-radius: 10px;
      max-width: 300px;
    }
    .product h3 {
      margin: 0 0 10px;
    }
    .product button {
      padding: 10px 20px;
      background-color: #444;
      color: #fff;
      border: none;
      border-radius: 5px;
      cursor: pointer;
    }
    .product button:hover {
      background-color: #555;
    }
  </style>
</head>
<body>
  <header>
    <h1>Онлайн Магазин IP Серверов</h1>
  </header>

  <nav>
    <a href="#purchases" onclick="showSection('purchases')">Покупки</a>
    <a href="#ip-servers" onclick="showSection('ip-servers')">IP Серверы</a>
  </nav>

  <div id="purchases" class="section active">
    <h2>Покупки</h2>
    <div class="product">
      <h3>Сервер 1</h3>
      <p>Цена: $10</p>
      <button>Купить</button>
    </div>
    <div class="product">
      <h3>Сервер 2</h3>
      <p>Цена: $15</p>
      <button>Купить</button>
    </div>
  </div>

  <div id="ip-servers" class="section">
    <h2>IP Серверы</h2>
    <p>Сервер 1: 192.168.0.1</p>
    <p>Сервер 2: 192.168.0.2</p>
  </div>

  <script>
    function showSection(id) {
      const sections = document.querySelectorAll('.section');
      sections.forEach(section => section.classList.remove('active'));
      document.getElementById(id).classList.add('active');
    }
  </script>
</body>
</html>
