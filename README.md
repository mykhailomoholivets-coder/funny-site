<!DOCTYPE html>
<html lang="ru">
<head>
  <meta charset="UTF-8" />
  <title>Генератор глупых предсказаний</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      text-align: center;
      background: linear-gradient(135deg, #ffe259, #ffa751);
      min-height: 100vh;
      margin: 0;
      padding: 40px;
    }

    .card {
      background: white;
      max-width: 600px;
      margin: auto;
      padding: 30px;
      border-radius: 25px;
      box-shadow: 0 10px 30px rgba(0,0,0,0.2);
    }

    h1 {
      font-size: 36px;
    }

    .face {
      font-size: 90px;
      animation: wiggle 1s infinite;
    }

    button {
      font-size: 20px;
      padding: 15px 25px;
      border: none;
      border-radius: 15px;
      background: #ff4d6d;
      color: white;
      cursor: pointer;
    }

    button:hover {
      transform: scale(1.08);
    }

    #result {
      margin-top: 25px;
      font-size: 24px;
      font-weight: bold;
    }

    @keyframes wiggle {
      0%, 100% { transform: rotate(-5deg); }
      50% { transform: rotate(5deg); }
    }
  </style>
</head>
<body>
  <div class="card">
    <div class="face">🧙‍♂️</div>
    <h1>Генератор глупых предсказаний</h1>
    <p>Нажми кнопку и узнай свою судьбу на сегодня!</p>

    <button onclick="predict()">Предсказать!</button>

    <div id="result">Твоя судьба пока спит 😴</div>
  </div>

  <script>
    const predictions = [
      "Сегодня тебя уважает даже твой холодильник.",
      "Через 5 минут ты захочешь печеньку. Это неизбежно.",
      "Твоя суперсила — забывать, зачем зашёл в комнату.",
      "Осторожно: носок может исчезнуть при стирке.",
      "Сегодня твой мозг работает в режиме картошки.",
      "Тебя ждёт великая победа над домашкой. Наверное.",
      "Кот где-то осуждает твои решения.",
      "Ты официально круче, чем вчерашний бутерброд."
    ];

    function predict() {
      const randomIndex = Math.floor(Math.random() * predictions.length);
      document.getElementById("result").textContent = predictions[randomIndex];
    }
  </script>
</body>
</html>
