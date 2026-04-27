<!DOCTYPE html>
<html lang="ru">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0"> <!-- Для мобильных устройств -->
  <title>Soulmate v4.0</title>
  <style>
    body {
      background: #0f172a;
      color: #e2e8f0;
      font-family: monospace;
      padding: 40px;
    }
    h1 { color: #38bdf8; }
    .block { margin-bottom: 30px; }
    .highlight { 
      color: #22c55e; 
      animation: pulse 2s infinite; /* Анимация пульсации */
    }
    @keyframes pulse {
      0% { opacity: 1; }
      50% { opacity: 0.5; }
      100% { opacity: 1; }
    }
    #secret { display: none; color: #ff69b4; } /* Скрытый блок */
    #secret img { max-width: 200px; height: auto; margin-top: 10px; } /* Стили для изображения */
    input, button { font-family: monospace; padding: 5px; }
  </style>
</head>
<body>

<h1>Soulmate System v4.0</h1>
<p class="highlight">Release: 4 years of connection ❤️</p>

<div class="block">
  <h2>System Log</h2>
  <p id="log-connection">connection: established</p>
  <p id="log-trust">trust: growing</p>
  <p id="log-distance">distance: ignored</p>
  <button onclick="rerunSystem()">Rerun System</button>
</div>

<div class="block">
  <h2>User Definitions</h2>
  <p>котик → ты</p>
  <p>птичка → Илья</p>
</div>

<div class="block">
  <h2>Soulmate Riddle</h2> <!-- Блок с загадкой -->
  <p>Загадка: Я — то, что соединяет котика и птичку, даже на расстоянии. Что я?</p>
  <input type="text" id="riddle-answer" placeholder="Ваш ответ">
  <button onclick="checkRiddle()">Проверить</button>
  <div id="secret">
    <p>Правильно! Connection unlocked! Мы — soulmates forever ❤️</p>
    <!-- Здесь добавлено предложенное изображение -->
    <img src="https://i.imgur.com/0tZ0ZfD.png" alt="Сердечко soulmate">
  </div>
</div>

<div class="block">
  <h2>Final</h2>
  <p>rerun()</p>
</div>

<script>
  // Функция для rerun (динамика)
  function rerunSystem() {
    const statuses = ['max', 'strong', 'eternal', 'zero', 'connected'];
    document.getElementById('log-trust').textContent = 'trust: ' + statuses[Math.floor(Math.random() * statuses.length)];
    document.getElementById('log-distance').textContent = 'distance: ' + statuses[Math.floor(Math.random() * statuses.length)];
    alert('System rerunned! New logs generated.');
  }

  // Функция для проверки загадки
  function checkRiddle() {
    const answer = document.getElementById('riddle-answer').value.toLowerCase();
    if (answer === 'любовь' || answer === 'love') { // Правильный ответ (на русском или английском)
      document.getElementById('secret').style.display = 'block';
    } else {
      alert('Неправильно! Подсказка: Это чувство, которое игнорирует расстояние.');
    }
  }
</script>

</body>
</html>
