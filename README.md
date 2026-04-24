<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Elio | Profile</title>

<style>
*{
  margin:0;
  padding:0;
  box-sizing:border-box;
}

body{
  font-family: Arial, Helvetica, sans-serif;
  background: linear-gradient(135deg,#0f172a,#111827,#1e293b);
  color:white;
  line-height:1.6;
}

header{
  text-align:center;
  padding:60px 20px 40px;
}

header h1{
  font-size:3rem;
  margin-bottom:10px;
}

header p{
  color:#cbd5e1;
  font-size:1.1rem;
}

.container{
  width:90%;
  max-width:1000px;
  margin:auto;
}

.card{
  background:rgba(255,255,255,0.05);
  border:1px solid rgba(255,255,255,0.08);
  border-radius:18px;
  padding:25px;
  margin-bottom:25px;
  backdrop-filter: blur(8px);
}

h2{
  margin-bottom:15px;
  color:#38bdf8;
}

ul{
  padding-left:20px;
}

li{
  margin-bottom:8px;
}

.stats{
  display:grid;
  grid-template-columns:repeat(auto-fit,minmax(200px,1fr));
  gap:15px;
}

.stat-box{
  background:rgba(255,255,255,0.04);
  padding:20px;
  border-radius:14px;
  text-align:center;
}

.stat-box h3{
  font-size:2rem;
  color:#22c55e;
}

button{
  padding:12px 18px;
  border:none;
  border-radius:10px;
  background:#38bdf8;
  color:white;
  font-weight:bold;
  cursor:pointer;
  margin-top:10px;
}

button:hover{
  background:#0ea5e9;
}

footer{
  text-align:center;
  padding:30px;
  color:#94a3b8;
}

.quote{
  margin-top:15px;
  font-style:italic;
  color:#facc15;
}
</style>
</head>

<body>

<header>
  <h1>Elio</h1>
  <p>Student • Tennis Player • Ambitious Builder</p>
</header>

<div class="container">

<div class="card">
  <h2>About Me</h2>
  <p>
    I'm Elio, a student-athlete focused on growth in academics, tennis, and life.
    I love tennis, self-improvement, competition, and building a strong future.
    I'm always looking for ways to level up.
  </p>
</div>

<div class="card">
  <h2>My Interests</h2>
  <ul>
    <li>🎾 Tennis (favorite sport)</li>
    <li>📚 School & learning</li>
    <li>💪 Performance & discipline</li>
    <li>📱 Tech and cool gear</li>
    <li>✝️ Faith</li>
  </ul>
</div>

<div class="card">
  <h2>Tennis Profile</h2>
  <ul>
    <li>Competitive mindset</li>
    <li>Focused on training and improvement</li>
    <li>Interested in gear, shoes, strings, and performance tools</li>
    <li>Long-term goals in tennis</li>
  </ul>
</div>

<div class="card">
  <h2>Current Goals</h2>
  <div class="stats">
    <div class="stat-box">
      <h3>100%</h3>
      <p>Commitment</p>
    </div>

    <div class="stat-box">
      <h3>Daily</h3>
      <p>Progress Mindset</p>
    </div>

    <div class="stat-box">
      <h3>Future</h3>
      <p>Big Goals</p>
    </div>
  </div>
</div>

<div class="card">
  <h2>Motivation Generator</h2>
  <p>Need a boost? Hit the button.</p>
  <button onclick="newQuote()">Generate</button>
  <p class="quote" id="quote">Your future is watching what you do today.</p>
</div>

</div>

<footer>
  Built by Elio on GitHub Pages 🚀
</footer>

<script>
const quotes = [
"Your future is watching what you do today.",
"Discipline beats motivation.",
"Pressure creates champions.",
"Keep stacking small wins.",
"One more rep. One more set. One more step.",
"Nobody can outwork consistency.",
"Dream big. Train bigger."
];

function newQuote(){
  let random = Math.floor(Math.random() * quotes.length);
  document.getElementById("quote").innerText = quotes[random];
}
</script>

</body>
</html>
