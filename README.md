<!DOCTYPE html>
<html lang="tr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Samet Çetinkuş | Cyber Security</title>

<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;500;700&display=swap" rel="stylesheet">

<style>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: 'Poppins', sans-serif;
    background: linear-gradient(135deg, #050505, #0d0d0d);
    color: white;
}

/* NAV */
nav {
    position: fixed;
    width: 100%;
    top: 0;
    padding: 20px 40px;
    display: flex;
    justify-content: space-between;
    background: rgba(0,0,0,0.6);
    backdrop-filter: blur(10px);
    z-index: 1000;
}

nav h1 {
    color: #00ffcc;
}

nav a {
    margin-left: 20px;
    color: #ccc;
    text-decoration: none;
    transition: 0.3s;
}

nav a:hover {
    color: #00ffcc;
}

/* HERO */
.hero {
    height: 100vh;
    display: flex;
    flex-direction: column;
    justify-content: center;
    padding: 0 10%;
}

.hero h2 {
    font-size: 50px;
    line-height: 1.2;
}

.hero h2 span {
    color: #00ffcc;
}

.hero p {
    margin-top: 20px;
    max-width: 600px;
    color: #aaa;
}

.btn {
    margin-top: 30px;
    display: inline-block;
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
    padding: 100px 10%;
}

/* GLASS CARD */
.card {
    background: rgba(255,255,255,0.05);
    border: 1px solid rgba(255,255,255,0.1);
    backdrop-filter: blur(15px);
    padding: 30px;
    border-radius: 15px;
    margin-top: 20px;
    transition: 0.4s;
}

.card:hover {
    transform: translateY(-5px);
    border-color: #00ffcc;
}

/* GRID */
.grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px,1fr));
    gap: 20px;
}

/* SKILLS */
.skills span {
    display: inline-block;
    margin: 5px;
    padding: 8px 15px;
    border: 1px solid #00ffcc;
    border-radius: 20px;
}

/* FOOTER */
footer {
    text-align: center;
    padding: 40px;
    color: #666;
}

/* SCROLL ANIMATION */
.hidden {
    opacity: 0;
    transform: translateY(40px);
    transition: all 1s;
}

.show {
    opacity: 1;
    transform: translateY(0);
}
</style>
</head>

<body>

<nav>
    <h1>Samet</h1>
    <div>
        <a href="#hakkimda">Hakkımda</a>
        <a href="#skill">Yetenekler</a>
        <a href="#iletisim">İletişim</a>
    </div>
</nav>

<div class="hero">
    <h2>Ben <span>Samet Çetinkuş</span><br>Cyber Security & Developer</h2>
    <p>
        6+ yıllık deneyimle siber güvenlik ve yazılım alanında aktif olarak çalışıyorum.
        Sistemleri sadece kullanmam — analiz eder, kırar ve yeniden inşa ederim.
    </p>
    <a href="#hakkimda" class="btn">Keşfet</a>
</div>

<section id="hakkimda" class="hidden">
    <h2>Hakkımda</h2>
    <div class="card">
        👋 Merhaba, ben Samet Çetinkuş.<br><br>

        Yaklaşık 6 yıldır bilişim teknolojileri alanında aktif olarak projeler geliştiriyor ve kendimi sürekli geliştirmeye odaklanıyorum.
        Bu süreçte hem pratik deneyim hem de teorik bilgi birikimi kazanarak siber güvenlik ve yazılım alanında uzmanlaştım.<br><br>

        Güvenli, ölçeklenebilir ve sürdürülebilir sistemler geliştirmek üzerine çalışıyorum.
        Zafiyet analizi, tehdit tespiti ve çözüm üretimi ana odak noktalarım.<br><br>

        <b>Nexora</b> kurucusu olarak gerçek dünya problemlerine profesyonel çözümler geliştiriyorum.
    </div>
</section>

<section id="skill" class="hidden">
    <h2>Teknolojiler</h2>

    <div class="skills">
        <span>Python</span>
        <span>C</span>
        <span>C#</span>
        <span>C++</span>
        <span>JavaScript</span>
        <span>PHP</span>
    </div>
</section>

<section class="hidden">
    <h2>Uzmanlık Alanları</h2>

    <div class="grid">
        <div class="card">Penetration Testing</div>
        <div class="card">Web Security</div>
        <div class="card">Network Security</div>
        <div class="card">Secure Coding</div>
    </div>
</section>

<section id="iletisim" class="hidden">
    <h2>İletişim</h2>
    <div class="card">
        Email: seninmailin@example.com
    </div>
</section>

<footer>
    © 2026 Samet Çetinkuş
</footer>

<script>
// SCROLL ANIMATION
const hiddenElements = document.querySelectorAll('.hidden');

const observer = new IntersectionObserver(entries => {
    entries.forEach(entry => {
        if(entry.isIntersecting){
            entry.target.classList.add('show');
        }
    });
});

hiddenElements.forEach(el => observer.observe(el));
</script>

</body>
</html>
