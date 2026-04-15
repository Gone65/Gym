
<!DOCTYPE html>
<html>
<head>
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>YOSA GYM</title>

<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&display=swap" rel="stylesheet">

<style>
*{
  margin:0;
  padding:0;
  box-sizing:border-box;
  font-family:'Poppins', sans-serif;
}

body{
  background:#0b0b0b;
  color:white;
}

/* NAVBAR */
.nav{
  position:sticky;
  top:0;
  display:flex;
  justify-content:space-between;
  padding:15px 20px;
  background:rgba(18,18,18,0.9);
  backdrop-filter:blur(8px);
}

.nav a{
  color:#ddd;
  margin:0 10px;
  text-decoration:none;
}

.nav a:hover{
  color:rgba(255,77,77,0.9);
}

/* HERO */
.hero{
  text-align:center;
  padding:70px 20px;
  background:linear-gradient(135deg,rgba(255,77,77,0.8),rgba(255,77,77,0.3));
}

.hero h1{
  font-size:40px;
}

/* BUTTON */
.btn{
  padding:12px 18px;
  margin:10px;
  border:1px solid rgba(255,77,77,0.6);
  background:rgba(255,77,77,0.1);
  color:white;
  border-radius:8px;
  cursor:pointer;
  transition:0.3s;
}

.btn:hover{
  background:white;
  color:black;
}

/* SECTIONS */
section{
  padding:50px 20px;
  text-align:center;
}

h2{
  color:rgba(255,77,77,0.9);
}

/* GRID */
.grid{
  display:grid;
  grid-template-columns:repeat(auto-fit,minmax(160px,1fr));
  gap:15px;
  margin-top:20px;
}

.card{
  background:rgba(255,255,255,0.03);
  padding:20px;
  border-radius:12px;
  border:1px solid rgba(255,77,77,0.2);
  cursor:pointer;
  transition:0.3s;
}

.card:hover{
  background:rgba(255,77,77,0.3);
  transform:translateY(-5px);
}

img{
  width:100%;
  max-width:500px;
  border-radius:12px;
  margin-top:20px;
}

/* PAGES */
.page{
  display:none;
  text-align:center;
}

.page.active{
  display:block;
}

/* CENTER FIX */
.page ul{
  list-style-position:inside;
  padding:0;
}

.page ul li{
  margin:10px 0;
}

.page img{
  display:block;
  margin:20px auto;
}

.page button{
  display:block;
  margin:20px auto;
}

/* TELEGRAM */
.telegram{
  position:fixed;
  bottom:15px;
  right:15px;
  background:#0088cc;
  color:white;
  padding:12px;
  border-radius:50px;
  text-decoration:none;
}

/* RESPONSIVE */
@media(max-width:768px){
  .nav{
    flex-direction:column;
    text-align:center;
  }
}
</style>
</head>

<body>

<!-- NAV -->
<div class="nav">
  <h2>YOSA GYM</h2>
  <div>
    <a href="#" onclick="showPage('home')">Home</a>
    <a href="#services">Services</a>
    <a href="#plans">Plans</a>
    <a href="#contact">Contact</a>
  </div>
</div>

<!-- HOME -->
<div id="home" class="page active">

  <div class="hero">
    <h1>YOSA GYM</h1>
    <p>Build Strength. Transform Your Body.</p>

    <button class="btn">Join Now</button>
    <button class="btn">Book Visit</button>
  </div>

  <!-- ABOUT -->
  <section>
    <h2>About YOSA GYM</h2>
    <p>A modern fitness center helping you build muscle and transform your life.</p>
    <img src="https://images.unsplash.com/photo-1558611848-73f7eb4001ab">
  </section>

  <!-- SERVICES -->
  <section id="services">
    <h2>Services</h2>
    <div class="grid">
      <div class="card" onclick="showPage('strength')">Strength Training</div>
      <div class="card" onclick="showPage('muscle')">Muscle Building</div>
      <div class="card" onclick="showPage('weight')">Weight Loss</div>
    </div>
  </section>

  <!-- PLANS -->
  <section id="plans">
    <h2>Membership Plans</h2>
    <div class="grid">
      <div class="card" onclick="showPage('basic')">Basic</div>
      <div class="card" onclick="showPage('standard')">Standard</div>
      <div class="card" onclick="showPage('premium')">Premium</div>
    </div>

    <img src="https://images.unsplash.com/photo-1599058917212-d750089bc07e">
  </section>

  <!-- CONTACT -->
  <section id="contact">
    <h2>Contact</h2>
    <p>Location: Addis Ababa</p>
    <p>Message us on Telegram to join</p>
  </section>

</div>

<!-- SERVICE PAGES -->
 <div id="strength" class="page">
<h1>Strength Training</h1>
<img src="https://images.unsplash.com/photo-1517836357463-d25dfeac3438">
<ul>
<li>Bench Press</li>
<li>Squats</li>
<li>Deadlift</li>
<li>Overhead Press</li>
</ul>
<button class="btn" onclick="showPage('home')">Back</button>
</div>

<div id="muscle" class="page">
<h1>Muscle Building</h1>
<img src="https://images.unsplash.com/photo-1594737625785-a6cbdabd333c">
<ul>
<li>Hypertrophy Training</li>
<li>Progressive Overload</li>
<li>High Protein Diet</li>
</ul>
<button class="btn" onclick="showPage('home')">Back</button>
</div>

<div id="weight" class="page">
<h1>Weight Loss</h1>
<img src="https://images.unsplash.com/photo-1554284126-aa88f22d8b74">
<ul>
<li>Cardio Training</li>
<li>Fat Burning Workouts</li>
<li>Calorie Control</li>
</ul>
<button class="btn" onclick="showPage('home')">Back</button>
</div>

<!-- PLAN PAGES -->

<div id="basic" class="page">
<h1>Basic Plan</h1>
<p>Access to all gym equipment.</p>
<button class="btn" onclick="showPage('home')">Back</button>
</div>

<div id="standard" class="page">
<h1>Standard Plan</h1>
<p>Gym + trainer guidance.</p>
<button class="btn" onclick="showPage('home')">Back</button>
</div>

<div id="premium" class="page">
<h1>Premium Plan</h1>
<p>VVIP coaching + meal plan.</p>
<button class="btn" onclick="showPage('home')">Back</button>
</div>

<!-- TELEGRAM -->
<a class="telegram" href="https://t.me/Yosiiyosi" target="_blank">
Telegram
</a>

<script>
function showPage(page){
  document.querySelectorAll('.page').forEach(p=>p.classList.remove('active'));
  document.getElementById(page).classList.add('active');
  window.scrollTo(0,0);
}
</script>

</body>
</html>
