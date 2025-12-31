<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Secret Confession</title>
<style>
  body {
    font-family: 'Arial', sans-serif;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    background: linear-gradient(135deg, #ffdde1, #ee9ca7);
    margin: 0;
    overflow: hidden;
  }

  .envelope {
    width: 350px;
    height: 220px;
    background: #e60026; /* Red envelope */
    position: relative;
    cursor: pointer;
    border-radius: 15px;
    box-shadow: 0 5px 20px rgba(0,0,0,0.3);
    display: flex;
    justify-content: center;
    align-items: center;
    text-align: center;
    padding: 20px;
    transition: transform 0.7s;
    color: #fff;
    font-weight: bold;
    font-size: 1.2em;
  }

  .envelope.open {
    transform: rotateX(180deg);
  }

  .message {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: #fff0f5;
    color: #d6336c;
    display: flex;
    justify-content: center;
    align-items: center;
    font-size: 1em;
    border-radius: 15px;
    opacity: 0;
    pointer-events: none;
    transition: opacity 0.5s;
    padding: 15px;
    box-sizing: border-box;
    overflow-y: auto;
    text-align: left;
  }

  .message.show {
    opacity: 1;
    pointer-events: auto;
  }

  .confetti {
    position: absolute;
    width: 10px;
    height: 10px;
    background: red;
    transform: rotate(45deg);
    animation: fall 3s linear infinite;
  }

  @keyframes fall {
    0% { transform: translateY(0) rotate(45deg); opacity:1; }
    100% { transform: translateY(500px) rotate(405deg); opacity:0; }
  }
</style>
</head>
<body>

<div class="envelope" id="envelope">
  Click me to open 💌
  <div class="message" id="message">
    <p>💖 Happy New Year! I know you don’t really know me… and I was planning on keeping it a secret until you noticed me. Hahaha, I know it’s kind of outrageous to confess through a website—it actually gave me a headache! But just so you know… I like you. Well… no, maybe it’s just a crush, a little admiration, and I definitely don’t want to give you any pressure. Uhmm… yeah, that’s it! I hope you have an amazing 2026!</p>
    <p>And… honestly, I don’t really know how to check if you saw this, so maybe leave a note on Messenger? Hahaha, it’s a request, not a command though. Again, byee! See you on my account when I get my degree, ikyk hehehheheh.</p>
    <p>From, Powtato 💖</p>
  </div>
</div>

<script>
const envelope = document.getElementById('envelope');
const message = document.getElementById('message');

function createConfetti() {
  const confetti = document.createElement('div');
  confetti.classList.add('confetti');
  confetti.style.left = Math.random() * window.innerWidth + 'px';
  confetti.style.background = `hsl(${Math.random()*360}, 70%, 60%)`;
  confetti.style.animationDuration = (2 + Math.random()*3) + 's';
  document.body.appendChild(confetti);
  setTimeout(() => confetti.remove(), 3000);
}

envelope.addEventListener('click', () => {
  envelope.classList.add('open');
  message.classList.add('show');
  
  // Generate confetti
  for(let i=0; i<50; i++) {
    setTimeout(createConfetti, i*50);
  }
});
</script>

</body>
</html>
# This-is-not-a-scam-open-me.
uhmm a secret 
