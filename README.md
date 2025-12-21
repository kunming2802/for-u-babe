<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>For U Babe 💕</title>

<style>
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;500&display=swap');

* {
  box-sizing: border-box;
  font-family: 'Poppins', sans-serif;
}

body {
  margin: 0;
  height: 100vh;
  background: linear-gradient(135deg, #ffd1dc, #ffe6f0);
  overflow: hidden;
  display: flex;
  justify-content: center;
  align-items: center;
}

.container {
  background: rgba(255,255,255,0.9);
  width: 90%;
  max-width: 520px;
  border-radius: 25px;
  padding: 20px;
  text-align: center;
  box-shadow: 0 10px 30px rgba(255,105,180,0.35);
}

h1 {
  color: #ff4f8b;
}

.song {
  background: #ffe6ef;
  border-radius: 15px;
  padding: 12px;
  margin: 10px 0;
  cursor: pointer;
  transition: 0.3s;
}

.song:hover {
  background: #ffb6c1;
  transform: scale(1.03);
}

.lyrics {
  display: none;
  background: #fff0f6;
  border-radius: 15px;
  padding: 10px;
  margin-top: 10px;
  font-size: 14px;
}

.spotify {
  display: inline-block;
  margin-top: 8px;
  padding: 6px 14px;
  background: #1DB954;
  color: white;
  border-radius: 20px;
  text-decoration: none;
  font-size: 13px;
}

/* floating hearts */
.heart {
  position: absolute;
  color: #ff69b4;
  font-size: 18px;
  animation: float 6s linear infinite;
  opacity: 0.7;
}

@keyframes float {
  0% {
    transform: translateY(100vh) scale(1);
    opacity: 0;
  }
  20% { opacity: 1; }
  100% {
    transform: translateY(-10vh) scale(1.5);
    opacity: 0;
  }
}
</style>
</head>

<body>

<div class="container">
  <h1>For U Babe 💖</h1>
  <p>Tap a song 🎧</p>

  <div class="song" onclick="toggleLyrics(1)">
    💕 All That I Know – Sabrina Carpenter
    <div class="lyrics" id="l1">
      All that I know is <br>
      I don't know how to be something you miss… <br>
      <a class="spotify" href="https://open.spotify.com/search/All%20That%20I%20Know%20Sabrina%20Carpenter" target="_blank">Open in Spotify</a>
    </div>
  </div>

  <div class="song" onclick="toggleLyrics(2)">
    💗 My Love Mine All Mine – Mitski
    <div class="lyrics" id="l2">
      My baby, my baby <br>
      You're my baby, say it to me… <br>
      <a class="spotify" href="https://open.spotify.com/search/My%20Love%20Mine%20All%20Mine%20Mitski" target="_blank">Open in Spotify</a>
    </div>
  </div>

  <div class="song" onclick="toggleLyrics(3)">
    💞 Better With You – Johnny Stimson
    <div class="lyrics" id="l3">
      Everything's better with you <br>
      I can't help but smile when you’re around… <br>
      <a class="spotify" href="https://open.spotify.com/search/Better%20With%20You%20Johnny%20Stimson" target="_blank">Open in Spotify</a>
    </div>
  </div>

  <div class="song" onclick="toggleLyrics(4)">
    💓 Double Take – Dhruv
    <div class="lyrics" id="l4">
      I could say I never dare to think about you… <br>
      But I know I’d go back to you… <br>
      <a class="spotify" href="https://open.spotify.com/search/Double%20Take%20Dhruv" target="_blank">Open in Spotify</a>
    </div>
  </div>

  <div class="song" onclick="toggleLyrics(5)">
    💘 Tip Toe – HYBS
    <div class="lyrics" id="l5">
      I don't wanna rush this moment <br>
      Let me tiptoe into your heart… <br>
      <a class="spotify" href="https://open.spotify.com/search/Tip%20Toe%20HYBS" target="_blank">Open in Spotify</a>
    </div>
  </div>
</div>

<script>
function toggleLyrics(n) {
  const lyric = document.getElementById("l" + n);
  lyric.style.display = lyric.style.display === "block" ? "none" : "block";
}

// floating hearts
setInterval(() => {
  const heart = document.createElement("div");
  heart.className = "heart";
  heart.innerHTML = "❤";
  heart.style.left = Math.random() * 100 + "vw";
  heart.style.animationDuration = 4 + Math.random() * 3 + "s";
  document.body.appendChild(heart);
  setTimeout(() => heart.remove(), 7000);
}, 300);
</script>

</body>
</html>