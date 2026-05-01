<!DOCTYPE html>
<html lang="tr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Samet | Cyber Security</title>

<style>
body {
    margin: 0;
    font-family: 'Courier New', monospace;
    background: black;
    color: #00ffcc;
    overflow-x: hidden;
}

/* MATRIX BACKGROUND */
canvas {
    position: fixed;
    top: 0;
    left: 0;
    z-index: -1;
}

/* HERO */
.hero {
    height: 100vh;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    text-align: center;

    animation: fadeIn 2s ease-in;
}

.hero h1 {
    font-size: 55px;
    letter-spacing: 3px;
}

.hero p {
    max-width: 700px;
    color: #aaa;
    margin-top: 20px;
    font-size: 18px;
}

/* BUTTON */
.btn {
    margin-top: 25px;
    padding: 12px 25px;
    border: 1px solid #00ffcc;
    color: #00ffcc;
    text-decoration: none;
    transition: 0.3s;
}

.btn:hover {
    background: #00ffcc;
    color: black;
}

/* SECTIONS */
section {
    padding: 80px 20px;
    max-width: 900px;
    margin: auto;
}

h2 {
    border-left: 4px solid #00ffcc;
    padding-left: 10px;
}

/* CARDS */
.card {
    background: rgba(0,0,0,0.7);
    border: 1px solid #00ffcc;
    padding: 20px;
    margin-top: 20px;
    transition: 0.3s;
}

.card:hover {
    transform: scale(1.03);
}

/* ANIMATION */
@keyframes fadeIn {
    from {opacity:0; transform: translateY(20px);}
    to {opacity:1; transform: translateY(0);}
}

/* GLITCH EFFECT */
.glitch {
    position: relative;
    color: #00ffcc;
}

.glitch::before,
.glitch::after {
    content: attr(data-text);
    position: absolute;
    left: 0;
}

.glitch::before {
    animation: glitchTop 1s infinite linear;
    color: red;
}

.glitch::after {
    animation: glitchBottom 1s infinite linear;
    color: blue;
}

@keyframes glitchTop {
    0% {clip-path: inset(0 0 80% 0);}
    50% {clip-path: inset(0 0 10% 0);}
    100% {clip-path: inset(0 0 80% 0);}
}

@keyframes glitchBottom {
    0% {clip-path: inset(80% 0 0 0);}
    50% {clip-path: inset(10% 0 0 0);}
    100% {clip-path: inset(80% 0 0 0);}
}

footer {
    text-align: center;
    padding: 20px;
    color: #555;
}
</style>
</head>

<body>

<canvas id="matrix"></canvas>

<div class="hero">
    <h1 class="glitch" data-text="SAMET ÇETİNKUŞ">SAMET ÇETİNKUŞ</h1>
    <p>
        Yaklaşık 6 yıldır bilişim teknolojileri alanında aktif olarak projeler geliştiriyorum.
        Siber güvenlik, yazılım geliştirme ve sistem analizi üzerine çalışıyorum.
        Amacım sadece sistemi kullanmak değil, sistemi çözmek.
    </p>
    <a href="#hakkimda" class="btn">Devam Et</a>
</div>

<section id="hakkimda">
    <h2>Hakkımda</h2>
    <p>
        Siber güvenlik benim için bir meslek değil, bir refleks.
        Açıkları görmek, sistemleri analiz etmek ve riskleri ortadan kaldırmak üzerine odaklanıyorum.
        Disiplinli, kararlı ve sonuç odaklı çalışırım.
    </p>
</section>

<section>
    <h2>Projeler</h2>

    <div class="card">
        <h3>Python Güvenlik Araçları</h3>
        <p>Otomasyon, analiz ve güvenlik testleri için özel araçlar geliştiriyorum.</p>
    </div>

    <div class="card">
        <h3>Siber Güvenlik Laboratuvarı</h3>
        <p>Gerçek dünya senaryoları üzerinden saldırı ve savunma çalışmaları yapıyorum.</p>
    </div>

</section>

<section>
    <h2>İletişim</h2>
    <p>Email: seninmailin@example.com</p>
</section>

<footer>
    <p>© 2026 Samet</p>
</footer>

<script>
// MATRIX EFFECT
const canvas = document.getElementById("matrix");
const ctx = canvas.getContext("2d");

canvas.height = window.innerHeight;
canvas.width = window.innerWidth;

const letters = "01";
const fontSize = 14;
const columns = canvas.width / fontSize;

const drops = [];
for(let x = 0; x < columns; x++) drops[x] = 1;

function draw(){
    ctx.fillStyle = "rgba(0,0,0,0.05)";
    ctx.fillRect(0,0,canvas.width,canvas.height);

    ctx.fillStyle = "#00ffcc";
    ctx.font = fontSize + "px monospace";

    for(let i=0; i<drops.length; i++){
        const text = letters.charAt(Math.floor(Math.random()*letters.length));
        ctx.fillText(text, i*fontSize, drops[i]*fontSize);

        if(drops[i]*fontSize > canvas.height && Math.random() > 0.975)
            drops[i] = 0;

        drops[i]++;
    }
}

setInterval(draw, 33);
</script>

</body>
</html>
