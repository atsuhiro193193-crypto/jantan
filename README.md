<!DOCTYPE html>
<html lang="ja">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>雀鍛</title>
  <style>
    * { box-sizing: border-box; }
    body{
      margin:0;
      background:#000;
      color:#fff;
      font-family:system-ui, sans-serif;
      padding:20px;
      text-align:center;
    }
    .title{
      font-size:42px;
      font-weight:900;
      color:#d4af37;
      margin-top:20px;
    }
    .sub{
      color:#ccc;
      margin-bottom:20px;
    }
    .card{
      background:#111;
      border:2px solid #d4af37;
      border-radius:20px;
      padding:20px;
      max-width:500px;
      margin:0 auto;
    }
    .hand{
      font-size:34px;
      line-height:1.8;
      margin:20px 0;
      word-break: break-word;
    }
    .choices{
      display:grid;
      grid-template-columns:1fr 1fr;
      gap:10px;
    }
    button{
      padding:16px;
      font-size:28px;
      border:none;
      border-radius:14px;
      background:#d4af37;
      color:#000;
      font-weight:700;
    }
    #result{
      margin-top:18px;
      font-size:22px;
      font-weight:700;
      min-height:32px;
    }
  </style>
</head>
<body>
  <div class="title">雀鍛</div>
  <div class="sub">勝つための麻雀トレーニング</div>

  <div class="card">
    <h2>何切るAI</h2>
    <div class="hand">🀇 🀈 🀉 🀋 🀋 🀌 🀍 🀙 🀚 🀛 🀐 🀐 🀄</div>

    <div class="choices">
      <button onclick="checkAnswer('🀇')">🀇</button>
      <button onclick="checkAnswer('🀋')">🀋</button>
      <button onclick="checkAnswer('🀐')">🀐</button>
      <button onclick="checkAnswer('🀄')">🀄</button>
    </div>

    <div id="result"></div>
  </div>

  <script>
    function checkAnswer(tile) {
      const result = document.getElementById('result');
      if (tile === '🀄') {
        result.textContent = '正解！ +50XP';
        result.style.color = '#ffd700';
      } else {
        result.textContent = '不正解… 正解は 🀄';
        result.style.color = '#ff5555';
      }
    }
  </script>
</body>
</html>
