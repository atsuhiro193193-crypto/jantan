<!DOCTYPE html>
<html lang="ja">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>雀鍛</title>
  <style>
    body{
      margin:0;
      background:#000;
      color:#fff;
      font-family:sans-serif;
      padding:20px;
      text-align:center;
    }
    .card{
      background:#111;
      border:2px solid #d4af37;
      border-radius:20px;
      padding:20px;
      margin-top:20px;
    }
    button{
      width:45%;
      margin:8px;
      padding:15px;
      font-size:28px;
      border:none;
      border-radius:14px;
      background:#d4af37;
      color:#000;
      font-weight:bold;
    }
    .title{
      font-size:42px;
      font-weight:900;
      color:#d4af37;
    }
  </style>
</head>
<body>
  <div class="title">雀鍛</div>
  <p>勝つための麻雀トレーニング</p>

  <div class="card">
    <h2>何切るAI</h2>
    <p style="font-size:34px;">🀇 🀈 🀉 🀋 🀋 🀌 🀍 🀙 🀚 🀛 🀐 🀐 🀄</p>
    <button onclick="check('🀇')">🀇</button>
    <button onclick="check('🀋')">🀋</button>
    <button onclick="check('🀐')">🀐</button>
    <button onclick="check('🀄')">🀄</button>
    <p id="result"></p>
  </div>

  <script>
    function check(tile){
      const result = document.getElementById('result');
      if(tile === '🀄'){
        result.innerHTML = '正解！ +50XP';
        result.style.color = '#ffd700';
      }else{
        result.innerHTML = '不正解… 正解は 🀄';
        result.style.color = '#ff5555';
      }
    }
  </script>
</body>
</html>
