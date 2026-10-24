
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Aleena's Six Seven Birthday ♡</title>

<style>
@import url('https://fonts.googleapis.com/css2?family=Nunito:wght@400;600;700;800;900&family=Pacifico&display=swap');

* { box-sizing: border-box; }

body {
  margin: 0;
  min-height: 100vh;
  font-family: 'Nunito', sans-serif;
  color: #8d496b;
  text-align: center;
  background: linear-gradient(145deg, #fff0f6, #ffe0ed, #fff5fa);
  overflow-x: hidden;
}

body::before {
  content: "♡  ✧  ♡  ✧  ♡  ✧  ♡";
  position: fixed;
  top: 12px;
  left: 0;
  width: 100%;
  color: #ed9cbe;
  font-size: 23px;
  letter-spacing: 18px;
  pointer-events: none;
}

.container {
  width: min(92%, 560px);
  margin: 0 auto;
  padding: 55px 0 35px;
}

h1 {
  font-family: 'Pacifico', cursive;
  font-size: clamp(30px, 8vw, 44px);
  font-weight: 400;
  color: #dc76a5;
  margin: 8px 0;
}

.subtitle {
  font-size: 14px;
  margin-bottom: 18px;
}

.cat-row {
  font-size: 35px;
  margin: 10px 0;
  animation: bob 2s infinite ease-in-out;
}

.card {
  background: rgba(255,255,255,.76);
  border: 2px solid #ffc9df;
  border-radius: 28px;
  padding: 22px 16px;
  box-shadow: 0 12px 30px #e9a1c526;
}

.instructions {
  min-height: 56px;
  font-size: 16px;
  font-weight: 800;
  margin: 5px auto 10px;
}

.cake-area {
  position: relative;
  height: 260px;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: flex-end;
  padding-bottom: 10px;
  margin: 12px 0;
}

.cake-top {
  position: absolute;
  top: 0;
  width: 100%;
  height: 100px;
  display: flex;
  justify-content: center;
  align-items: flex-end;
  gap: 7px;
  z-index: 3;
}

.digit {
  font-size: 76px;
  font-weight: 900;
  line-height: 1;
  color: #ff6f9f;
  text-shadow: 2px 3px 0 #ffbdd4;
  position: relative;
  animation: pop .45s ease;
}

.digit::before {
  content: "🔥";
  font-size: 19px;
  position: absolute;
  top: -20px;
  left: 50%;
  transform: translateX(-50%);
}

.digit.no-flame::before {
  content: "";
}

.cake {
  position: relative;
  width: 240px;
  height: 110px;
  border-radius: 18px 18px 25px 25px;
  background: #f6a9ca;
  border-bottom: 9px solid #e77eac;
  box-shadow: inset 0 -8px 0 #f08bb8;
  z-index: 2;
}

.frosting {
  position: absolute;
  top: -12px;
  left: 0;
  width: 100%;
  height: 32px;
  border-radius: 50%;
  background: #fff9fc;
  border-bottom: 5px solid #ffd3e5;
}

.drip {
  position: absolute;
  top: 8px;
  width: 18px;
  height: 20px;
  border-radius: 0 0 12px 12px;
  background: #fff9fc;
}

.drip.one { left: 38px; height: 28px; }
.drip.two { left: 104px; height: 19px; }
.drip.three { right: 38px; height: 31px; }

.sprinkles {
  position: absolute;
  top: 42px;
  left: 0;
  width: 100%;
  font-size: 19px;
  letter-spacing: 8px;
}

.plate {
  width: 285px;
  height: 22px;
  border-radius: 50%;
  background: #fff;
  border: 3px solid #ffc9df;
  margin-top: -2px;
  z-index: 1;
}

.moved-six {
  position: absolute;
  right: 20px;
  top: 30px;
  padding: 8px 13px;
  background: #fff;
  border: 2px dashed #f5a4c7;
  border-radius: 16px;
  font-size: 13px;
  font-weight: 800;
  transform: rotate(8deg);
  animation: pop .45s ease;
}

.moved-six span {
  display: block;
  font-size: 33px;
  color: #ff6f9f;
}

button {
  font-family: inherit;
  font-size: 15px;
  font-weight: 900;
  border: none;
  border-radius: 999px;
  padding: 13px 19px;
  margin: 5px;
  cursor: pointer;
  transition: transform .2s, box-shadow .2s;
}

button:hover {
  transform: translateY(-2px);
  box-shadow: 0 5px 12px #d979a744;
}

.primary {
  color: white;
  background: linear-gradient(135deg, #f18db7, #e875a6);
}

.secondary {
  color: #c55d8e;
  background: #ffe0ed;
}

button:disabled {
  opacity: .45;
  cursor: not-allowed;
  transform: none;
}

.message {
  display: none;
  margin-top: 22px;
  padding: 20px 14px;
  border-radius: 22px;
  background: #fff0f7;
  border: 2px dashed #f2a4c7;
  animation: pop .6s ease;
}

.message h2 {
  font-family: 'Pacifico', cursive;
  font-weight: 400;
  font-size: 29px;
  color: #df76a5;
}

.message p {
  line-height: 1.8;
  font-size: 15px;
}

.footer {
  font-size: 12px;
  margin-top: 17px;
  opacity: .75;
}

.floating-cat {
  position: fixed;
  font-size: 27px;
  pointer-events: none;
  animation: float 5s ease-in-out infinite;
  opacity: .7;
}

.cat1 { top: 20%; left: 3%; }
.cat2 { top: 53%; right: 3%; animation-delay: 1s; }
.cat3 { bottom: 8%; left: 7%; animation-delay: 2s; }
.cat4 { bottom: 15%; right: 8%; animation-delay: .5s; }

.confetti {
  position: fixed;
  top: -30px;
  z-index: 10;
  pointer-events: none;
  animation: fall 2.8s linear forwards;
}

@keyframes bob {
  0%,100% { transform: translateY(0); }
  50% { transform: translateY(-6px); }
}

@keyframes float {
  0%,100% { transform: translateY(0) rotate(-8deg); }
  50% { transform: translateY(-17px) rotate(8deg); }
}

@keyframes pop {
  0% { transform: scale(.7); opacity: 0; }
  100% { transform: scale(1); opacity: 1; }
}

@keyframes fall {
  to { transform: translateY(110vh) rotate(650deg); opacity: 0; }
}

@media (max-width: 400px) {
  .cake { width: 210px; }
  .plate { width: 250px; }
  .moved-six { right: 0; }
}
</style>
</head>

<body>
<div class="floating-cat cat1">🐱</div>
<div class="floating-cat cat2">🎀</div>
<div class="floating-cat cat3">🐾</div>
<div class="floating-cat cat4">🐈</div>

<main class="container">
  <div class="cat-row">🎀 🐱 🎂 🐱 🎀</div>
  <h1>Happy birthday Aleena ♡</h1>
  <p class="subtitle">the six seven cake moment you deserved 😭</p>

  <section class="card">
    <p class="instructions" id="instructions">
      ALRIGHT, YOUR CAKE IS READY BIG DAWG 🥹<br>
      let's do this properly.
    </p>

    <div class="cake-area">
      <div class="cake-top" id="cakeNumber">
        <span class="digit">1</span>
        <span class="digit">6</span>
      </div>

      <div class="cake">
        <div class="frosting"></div>
        <div class="drip one"></div>
        <div class="drip two"></div>
        <div class="drip three"></div>
        <div class="sprinkles">🍓 ✦ 🍓 ✦ 🍓</div>
      </div>
      <div class="plate"></div>
      <div id="movedSix"></div>
    </div>

    <button class="primary" id="nextButton" onclick="nextStep()">
      take the 6 out ✋
    </button>

    <button class="secondary" onclick="resetCake()">
      start over ↻
    </button>

    <div class="message" id="birthdayMessage">
      <div style="font-size:35px">🎂 🐱 💗 🐱 🎂</div>
      <h2>Aleenaaaaa 🥹♡</h2>
      <p>
        you didn't get to do ur 67 cake stuff cuz of ur mom,
        but dw i gotchu bruh so here's ur own lil redo <br><br>
        i hope this next year brings you so much happiness,
        so many good memories, and everything you've been wishing for.
        you deserve to have your little moments of joy, always.<br><br>
        Happy belated birthday bro 🎀<br>
        <b>lmk when ur mom pissed u off again. imma bha. I love you, alright. ♡</b>
      </p>
      <button class="primary" onclick="resetCake()">do it again!! 🎂</button>
    </div>
  </section>

  <p class="footer">made with so much love, just for you ♡</p>
</main>

<script>
let step = 0;
let candlesOut = false;

const instructions = document.getElementById("instructions");
const cakeNumber = document.getElementById("cakeNumber");
const movedSix = document.getElementById("movedSix");
const nextButton = document.getElementById("nextButton");
const birthdayMessage = document.getElementById("birthdayMessage");

function showNumber(number, flames = true) {
  cakeNumber.innerHTML = [...String(number)].map(digit =>
    `<span class="digit ${flames ? "" : "no-flame"}">${digit}</span>`
  ).join("");
}

function say67() {
  // Stop any previous speech, then have the computer say "67!"
  if ("speechSynthesis" in window) {
    window.speechSynthesis.cancel();

    const speech = new SpeechSynthesisUtterance("six seven!");
    speech.rate = 0.85;
    speech.pitch = 1.25;
    speech.volume = 1;

    window.speechSynthesis.speak(speech);
  }
}

function nextStep() {
  step++;

  if (step === 1) {
    // Take the 6 away from 16
    showNumber("1");
    movedSix.innerHTML = '<div class="moved-six">we got the 6!<span>6</span></div>';
    instructions.innerHTML = "first take the 6 out of 16";
    nextButton.textContent = "bring the 7 over";
  }

  else if (step === 2) {
    // Put 6 and 7 together to make 67
    showNumber("67");
    movedSix.innerHTML = "";
    instructions.innerHTML = "NOW PUT THE 7 BESIDE THE 6";
    nextButton.textContent = "SIX SEVENNNN 🗣️‼️ ";
  }

  else if (step === 3) {
    // The big 67 moment!
    showNumber("67");
    instructions.innerHTML = "SIX SEVENNNNNNN 🗣️‼️";
    say67();
    confetti();
    nextButton.textContent = "put the 7 beside the 1";
  }

  else if (step === 4) {
    // Move 7 beside 1 to make 17
    showNumber("17");
    instructions.innerHTML = "AND NOW THE 7 GOES BESIDE THE 1... 17!";
    confetti();
    nextButton.textContent = "blow the candles out";
  }

  else if (step === 5) {
    // Blow out the candles and reveal the birthday message
    showNumber("17", false);
    candlesOut = true;
    instructions.innerHTML = "make a wish, aleena. 💗";
    nextButton.style.display = "none";
    birthdayMessage.style.display = "block";
    confetti();
  }
}

function resetCake() {
  step = 0;
  candlesOut = false;
  showNumber("16");
  movedSix.innerHTML = "";
  instructions.innerHTML =
    "ALRIGHT, YOUR CAKE IS READY BIG DAWG 🥹<br>let's do this properly.";
  nextButton.style.display = "inline-block";
  nextButton.textContent = "take the 6 out";
  birthdayMessage.style.display = "none";

  if ("speechSynthesis" in window) {
    window.speechSynthesis.cancel();
  }
}

function confetti() {
  const pieces = ["💗", "🎀", "✨", "🌸", "💕", "🐾"];

  for (let i = 0; i < 32; i++) {
    const piece = document.createElement("div");
    piece.className = "confetti";
    piece.textContent = pieces[Math.floor(Math.random() * pieces.length)];
    piece.style.left = Math.random() * 100 + "vw";
    piece.style.animationDelay = Math.random() * 0.9 + "s";
    piece.style.fontSize = (14 + Math.random() * 16) + "px";
    document.body.appendChild(piece);
    setTimeout(() => piece.remove(), 4000);
  }
}
</script>
</body>
</html>
