<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>NeroInvestPro – Smarter Investments</title>

  <style>
/* ------------------------------ GLOBAL STYLES ------------------------------ */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: "Poppins", sans-serif;
}

body {
  background: #f5f7fa;
  color: #1b1b1b;
  overflow-x: hidden;
}

/* ------------------------------ NAVIGATION ------------------------------ */
.nav {
  width: 100%;
  background: #0b1a34;
  padding: 18px 40px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  position: fixed;
  top: 0;
  z-index: 1000;
  animation: slideDown 0.7s ease;
}

@keyframes slideDown {
  from { transform: translateY(-50px); opacity: 0; }
  to { transform: translateY(0); opacity: 1; }
}

.nav-logo {
  font-size: 26px;
  font-weight: 700;
  color: #4ac1ff;
}

.nav-links {
  display: flex;
  align-items: center;
  gap: 25px;
}

.nav-links a {
  color: #dce7ff;
  text-decoration: none;
  font-size: 16px;
  transition: 0.3s;
}

.nav-links a:hover {
  color: #4ac1ff;
  transform: translateY(-2px);
}

/* Login Button */
.nav-btn {
  background: #4ac1ff;
  padding: 10px 22px;
  border-radius: 8px;
  color: #002244;
  font-weight: 600;
}

.nav-btn:hover {
  background: #78d5ff;
}

/* Mobile Toggle */
.nav-toggle {
  display: none;
  flex-direction: column;
  cursor: pointer;
  gap: 5px;
}

.nav-toggle span {
  width: 28px;
  height: 3px;
  background: #fff;
  border-radius: 2px;
}

/* Mobile View */
@media(max-width: 820px) {
  .nav-links {
    position: absolute;
    top: 70px;
    right: -100%;
    background: #0b1a34;
    flex-direction: column;
    width: 220px;
    padding: 20px;
    transition: 0.4s ease;
  }

  .nav-links.active {
    right: 0;
  }

  .nav-toggle {
    display: flex;
  }
}

/* ------------------------------ HERO ------------------------------ */
.hero {
  padding: 180px 40px 120px;
  text-align: center;
  color: white;
  background-image: url("images/investment.png");
  background-size: cover;
  background-position: center;
  position: relative;
}

.hero::before {
  content: "";
  position: absolute;
  inset: 0;
  background: rgba(0, 0, 0, 0.45);
}

.hero h1,
.hero p,
.hero .btn {
  position: relative;
  z-index: 2;
}

.hero h1 {
  font-size: 50px;
  font-weight: 700;
  animation: fadeUp 1s ease forwards;
}

.hero p {
  margin-top: 10px;
  font-size: 20px;
  opacity: 0.9;
  animation: fadeUp 1.3s ease forwards;
}

@keyframes fadeUp {
  from { opacity: 0; transform: translateY(20px); }
  to { opacity: 1; transform: translateY(0); }
}

.hero .btn {
  background: #4ac1ff;
  padding: 15px 35px;
  font-size: 18px;
  color: #002244;
  border-radius: 8px;
  margin-top: 25px;
  text-decoration: none;
  transition: 0.3s;
}

.hero .btn:hover {
  background: #78d5ff;
  transform: scale(1.05);
}

/* ------------------------------ PLANS ------------------------------ */
.plans {
  padding: 100px 40px;
  text-align: center;
}

.plans h2 {
  font-size: 36px;
  margin-bottom: 40px;
}

.plan-container {
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
  gap: 25px;
}

.plan-card {
  background: white;
  width: 300px;
  padding: 25px;
  border-radius: 14px;
  box-shadow: 0 8px 20px rgba(0,0,0,0.15);
  transition: 0.35s;
}

.plan-card:hover {
  transform: translateY(-8px);
  box-shadow: 0 12px 28px rgba(0,0,0,0.2);
}

.plan-card h3 {
  color: #003366;
  margin-bottom: 10px;
}

.plan-card button {
  margin-top: 15px;
  padding: 10px 20px;
  background: #4ac1ff;
  color: #002244;
  border-radius: 8px;
  cursor: pointer;
  border: none;
}

.plan-card button:hover {
  background: #78d5ff;
}

/* ------------------------------ MINING SECTION ------------------------------ */
.mining-section {
  padding: 100px 40px;
  text-align: center;
  background: #eef6ff;
  margin-top: 40px;
}

.mining-box {
  width: 90%;
  max-width: 600px;
  background: white;
  margin: 0 auto;
  padding: 30px;
  border-radius: 14px;
  box-shadow: 0 8px 20px rgba(0,0,0,0.1);
}

#miningProgress {
  width: 100%;
  height: 20px;
  background: #dbeaff;
  border-radius: 12px;
  margin-top: 15px;
  overflow: hidden;
}

#miningBar {
  height: 100%;
  width: 0%;
  background: linear-gradient(90deg, #4ac1ff, #0077ff);
  transition: width 0.2s;
}

.console {
  background: #000;
  color: #4aff6a;
  padding: 12px;
  height: 120px;
  overflow-y: auto;
  margin-top: 20px;
  font-family: monospace;
  border-radius: 8px;
  font-size: 13px;
}

.mining-btn {
  margin-top: 20px;
  padding: 12px 30px;
  background: #0077ff;
  color: white;
  border: none;
  font-size: 17px;
  border-radius: 8px;
  cursor: pointer;
  font-weight: 600;
}

.mining-btn:hover {
  background: #4ac1ff;
}

/* ------------------------------ FOOTER ------------------------------ */
footer {
  text-align: center;
  padding: 22px;
  background: #0b1a34;
  color: #dce7ff;
  margin-top: 60px;
}
  </style>

</head>

<body>

<!-- NAVIGATION -->
<header class="nav">
  <div class="nav-logo">NeroInvestPro</div>

<nav class="nav-links" id="navLinks">
  <a href="index.html">Home</a>
  <a href="plans.html">Plans</a>
  <a href="dashboard.html">Dashboard</a>
  <a href="mining.html">Mining</a>
  <a href="login.html" class="nav-btn">Login</a>
</nav>

  <div class="nav-toggle" id="navToggle">
    <span></span>
    <span></span>
    <span></span>
  </div>
</header>

<!-- HERO -->
<section class="hero">
  <h1>Grow Your Wealth with Smart Investments</h1>
  <p>Join thousands of investors earning steady returns with our trusted investment plans.</p>
  <a href="#plans" class="btn">View Investment Plans</a>
</section>

<!-- PLANS -->
<section id="plans" class="plans">
  <h2>Investment Plans</h2>

  <div class="plan-container">

    <div class="plan-card">
      <h3>Starter Plan</h3>
      <p>ROI: 10% / Month</p>
      <p>Min Deposit: $100</p>
      <button>Invest Now</button>
    </div>

    <div class="plan-card">
      <h3>Growth Plan</h3>
      <p>ROI: 18% / Month</p>
      <p>Min Deposit: $500</p>
      <button>Invest Now</button>
    </div>

    <div class="plan-card">
      <h3>Pro Plan</h3>
      <p>ROI: 25% / Month</p>
      <p>Min Deposit: $1000</p>
      <button>Invest Now</button>
    </div>

  </div>
</section>

<!-- MINING SYSTEM -->
<section id="mining" class="mining-section">
  <h2>⛏ Demo Mining System</h2>
  <p>Experience how our automated mining algorithm works in real time.</p>

  <div class="mining-box">
    <h3>Mining Progress</h3>

    <div id="miningProgress">
      <div id="miningBar"></div>
    </div>

    <p style="margin-top:10px;">Earnings: <strong id="earnings">$0.00</strong></p>

    <div class="console" id="consoleBox">
      ▶ Ready to start mining...
    </div>

    <button class="mining-btn" id="startMining">Start Demo Mining</button>
  </div>
</section>

<!-- FOOTER -->
<footer>
  © 2025 NeroInvestPro. All Rights Reserved.
</footer>

<!-- SCRIPTS -->
<script>
/* Mobile Menu */
const navToggle = document.getElementById("navToggle");
const navLinks = document.getElementById("navLinks");

navToggle.addEventListener("click", () => {
  navLinks.classList.toggle("active");
});

/* Mining System Script */
const startBtn = document.getElementById("startMining");
const miningBar = document.getElementById("miningBar");
const consoleBox = document.getElementById("consoleBox");
const earningsText = document.getElementById("earnings");

let mining = false;

startBtn.addEventListener("click", () => {
  if (mining) return;

  mining = true;
  miningBar.style.width = "0%";
  consoleBox.innerHTML = "";

  let progress = 0;
  let earnings = 0;

  const miningProcess = setInterval(() => {
    progress += 2;
    earnings += (Math.random() * 0.5);

    miningBar.style.width = progress + "%";
    earningsText.innerText = "$" + earnings.toFixed(2);

    consoleBox.innerHTML += "⛏ Mining block... " + progress + "%<br>";
    consoleBox.scrollTop = consoleBox.scrollHeight;

    if (progress >= 100) {
      clearInterval(miningProcess);
      consoleBox.innerHTML += "<br>✔ Mining complete!<br>";
      mining = real ;
    }
  }, 200);
});
</script>

</body>
</html>

