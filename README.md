<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Elio | Student Profile</title>

<style>
*{
  margin:0;
  padding:0;
  box-sizing:border-box;
  scroll-behavior:smooth;
}

body{
  font-family: Arial, Helvetica, sans-serif;
  background:#0f172a;
  color:white;
}

/* NAVBAR */
nav{
  position:fixed;
  width:100%;
  top:0;
  background:rgba(0,0,0,0.6);
  backdrop-filter: blur(8px);
  padding:15px;
  display:flex;
  justify-content:space-between;
  align-items:center;
}

nav h1{
  font-size:1.2rem;
}

nav a{
  color:white;
  text-decoration:none;
  margin-left:15px;
  font-size:0.9rem;
}

/* SECTIONS */
section{
  padding:100px 20px;
  max-width:900px;
  margin:auto;
}

h2{
  margin-bottom:15px;
  color:#38bdf8;
}

.card{
  background:rgba(255,255,255,0.05);
  padding:20px;
  border-radius:15px;
  margin-top:15px;
}

/* HERO */
.hero{
  text-align:center;
  padding-top:140px;
}

.hero h1{
  font-size:3rem;
}

.hero p{
  color:#94a3b8;
}

/* BUTTON */
button{
  margin-top:10px;
  padding:10px 15px;
  border:none;
  border-radius:8px;
  background:#38bdf8;
  color:white;
  cursor:pointer;
}

button:hover{
  background:#0ea5e9;
}

/* INPUT */
input{
  padding:8px;
  margin:5px;
  border-radius:6px;
  border:none;
}

/* DARK MODE */
.light{
  background:white;
  color:black;
}

.light .card{
  background:#f1f5f9;
}

footer{
  text-align:center;
  padding:30px;
  color:#94a3b8;
}
</style>
</head>

<body>

<nav>
  <h1>Elio</h1>
  <div>
    <a href="#about">About</a>
    <a href="#tennis">Tennis</a>
    <a href="#tracker">Tracker</a>
    <a href="#contact">Contact</a>
    <button onclick="toggleMode()">🌙</button>
  </div>
</nav>

<section class="hero">
  <h1>Elio</h1>
  <p>Student • Tennis Player • Focused on Growth</p>
</section>

<section id="about">
  <h2>About Me</h2>
  <div class="card">
    <p>
      I'm a student-athlete focused on improving every day.
      I care about discipline, performance, and building a strong future.
    </p>
  </div>
</section>

<section id="tennis">
  <h2>Tennis</h2>
  <div class="card">
    <p>
      Competitive player working on consistency, training, and long-term development.
      Interested in gear, performance, and improving every part of my game.
    </p>
  </div>
</section>

<section id="tracker">
  <h2>Training Tracker</h2>
  <div class="card">
    <p>Log your daily work:</p>

    <input type="number" id="hours" placeholder="Hours trained">
    <input type="number" id="sleep" placeholder="Sleep hours">

    <br>

    <button onclick="saveData()">Save</button>

    <p id="savedData"></p>
  </div>
</section>

<section id="contact">
  <h2>Contact</h2>
  <div class="card">
    <p>Email: your@email.com</p>
  </div>
</section>

<footer>
  Built by Elio 🚀
</footer>

<script>
function toggleMode(){
  document.body.classList.toggle("light");
}

function saveData(){
  let hours = document.getElementById("hours").value;
  let sleep = document.getElementById("sleep").value;

  localStorage.setItem("hours", hours);
  localStorage.setItem("sleep", sleep);

  document.getElementById("savedData").innerText =
    "Saved: " + hours + " hrs training, " + sleep + " hrs sleep";
}

/* Load saved data */
window.onload = function(){
  let hours = localStorage.getItem("hours");
  let sleep = localStorage.getItem("sleep");

  if(hours && sleep){
    document.getElementById("savedData").innerText =
      "Last entry: " + hours + " hrs training, " + sleep + " hrs sleep";
  }
}
</script>

</body>
</html>
