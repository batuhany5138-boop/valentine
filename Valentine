<!doctype html>
<html lang="de">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Will you be my Valentine, Selin?</title>
  <style>
    :root { --bg:#0b0b10; --card:#141423; --txt:#f3f3ff; --muted:#b7b7d6; }
    body{
      margin:0; min-height:100vh; display:grid; place-items:center;
      background: radial-gradient(1200px 600px at 50% 20%, #2b2b60 0%, var(--bg) 55%);
      font-family: system-ui, -apple-system, Segoe UI, Roboto, Arial, sans-serif;
      color:var(--txt);
    }
    .card{
      width:min(560px, 92vw);
      background: color-mix(in oklab, var(--card) 92%, black 8%);
      border:1px solid rgba(255,255,255,.08);
      border-radius:20px;
      padding:28px 22px;
      box-shadow: 0 16px 60px rgba(0,0,0,.5);
      text-align:center;
      position:relative;
      overflow:hidden;
    }
    h1{ margin:0 0 10px; font-size: clamp(22px, 4.5vw, 34px); }
    p{ margin:0 0 18px; color:var(--muted); }
    .btns{ display:flex; justify-content:center; gap:12px; flex-wrap:wrap; }
    button{
      border:0; border-radius:14px; padding:12px 18px; font-size:16px;
      cursor:pointer; transition: transform .08s ease;
    }
    button:active{ transform: scale(.98); }
    .yes{ background: #ff4d7d; color:white; }
    .no{ background: rgba(255,255,255,.10); color:var(--txt); position:relative; }
    .small{ font-size:12px; opacity:.85; margin-top:14px; }
    .msg{
      display:none; margin-top:18px; padding:16px;
      border-radius:16px; background: rgba(255,255,255,.06);
      border:1px solid rgba(255,255,255,.10);
    }
    .heart{
      position:absolute; inset:auto; width:14px; height:14px;
      transform: rotate(45deg);
      background:#ff4d7d;
      opacity:.85;
      border-radius:3px;
      animation: float 2.2s ease-out forwards;
      pointer-events:none;
    }
    .heart::before, .heart::after{
      content:""; position:absolute; width:14px; height:14px;
      border-radius:50%; background:#ff4d7d;
      top:-7px; left:0;
    }
    .heart::after{ left:-7px; top:0; }
    @keyframes float{
      from{ transform: translateY(0) rotate(45deg); opacity:.9; }
      to{ transform: translateY(-140px) rotate(45deg); opacity:0; }
    }
  </style>
</head>
<body>
  <div class="card">
    <h1 id="title">Will you be my Valentine, Selin? 💘</h1>
    <p id="subtitle">Ich wollte dich schon lange etwas fragen… 🥺👉👈</p>

    <div class="btns">
      <button class="yes" id="yesBtn">Ja 💖</button>
      <button class="no" id="noBtn">Nein 🙈</button>
    </div>

    <div class="msg" id="msg">
      <h2 style="margin:0 0 6px;">Yaaay! 🥰</h2>
      <p style="margin:0;">Dann bist du offiziell mein Valentine, Selin. 💞</p>
      <p style="margin:10px 0 0; color:var(--muted);">Schick mir ein ❤️ zurück: <strong>„JA!! – Batu 💘“</strong></p>
    </div>

    <div class="small">Made with ❤️ by Batu</div>
  </div>

  <script>
    const yesBtn = document.getElementById("yesBtn");
    const noBtn = document.getElementById("noBtn");
    const msg = document.getElementById("msg");
    const subtitle = document.getElementById("subtitle");

    function popHearts(count = 12) {
      const card = document.querySelector(".card");
      for (let i = 0; i < count; i++) {
        const h = document.createElement("div");
        h.className = "heart";
        const x = Math.random() * 100;
        const delay = Math.random() * 0.4;
        h.style.left = x + "%";
        h.style.bottom = "-10px";
        h.style.animationDelay = delay + "s";
        card.appendChild(h);
        setTimeout(() => h.remove(), 2600);
      }
    }

    yesBtn.addEventListener("click", () => {
      msg.style.display = "block";
      subtitle.textContent = "Ich wusste es 😎💞";
      popHearts(16);
      noBtn.disabled = true;
      noBtn.style.opacity = 0.5;
      noBtn.style.cursor = "not-allowed";
    });

    // "Nein" weicht aus 😏
    noBtn.addEventListener("mouseenter", moveNo);
    noBtn.addEventListener("click", moveNo);

    function moveNo() {
      const card = document.querySelector(".card");
      const rect = card.getBoundingClientRect();
      const btnRect = noBtn.getBoundingClientRect();

      const maxX = rect.width - btnRect.width - 20;
      const maxY = rect.height - btnRect.height - 20;

      const x = Math.random() * maxX;
      const y = Math.random() * maxY;

      noBtn.style.position = "absolute";
      noBtn.style.left = x + "px";
      noBtn.style.top = y + "px";
    }
  </script>
</body>
</html>
