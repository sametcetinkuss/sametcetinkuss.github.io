<!DOCTYPE html>
<html lang="tr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Samet Çetinkuş | Cyber Security</title>

<link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700&display=swap" rel="stylesheet">

<style>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: 'Inter', sans-serif;
    background: linear-gradient(135deg, #0f172a, #020617);
    color: #e2e8f0;
}

/* NAV */
nav {
    position: fixed;
    width: 100%;
    padding: 20px 8%;
    display: flex;
    justify-content: space-between;
    background: rgba(2,6,23,0.7);
    backdrop-filter: blur(12px);
    border-bottom: 1px solid rgba(255,255,255,0.05);
}

nav h1 {
    color: #38bdf8;
}

nav a {
    margin-left: 25px;
    text-decoration: none;
    color: #94a3b8;
    font-size: 14px;
}

nav a:hover {
    color: #38bdf8;
}

/* HERO */
.hero {
    height: 100vh;
    display: flex;
    align-items: center;
    padding: 0 8%;
}

.hero-content {
    max-width: 700px;
}

.hero h2 {
    font-size: 52px;
    font-weight: 700;
    line-height: 1.2;
}

.hero h2 span {
    color: #38bdf8;
}

.hero p {
    margin-top: 20px;
    color: #94a3b8;
    line-height: 1.7;
}

/* BUTTON */
.btn {
    margin-top: 30px;
    display: inline-block;
    padding: 12px 24px;
    background: #38bdf8;
    color: #020617;
    border-radius: 8px;
    text-decoration: none;
    font-weight: 600;
}

.btn:hover {
    background: #0ea5e9;
}

/* SECTION */
section {
    padding: 100px 8%;
}

/* CARD */
.card {
    background: rgba(255,255,255,0.03);
    border: 1px solid rgba(255,255,255,0.05);
    border-radius: 12px;
    padding: 30px;
    margin-top: 20px;
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
    margin: 6px;
    padding: 8px 14px;
    background: rgba(56,189,248,0.1);
    border-radius: 20px;
    font-size: 13px;
}

/* FOOTER */
footer {
    text-align: center;
    padding: 40px;
    color: #64748b;
}
</style>
</head>

<body>

<nav>
    <h1>Samet</h1>
    <div>
        <a href="#hakkimda">Hakkımda</a>
        <a href="#yetenek">Yetenekler</a>
        <a href="#iletisim">İletişim</a>
    </div>
</nav>

<div class="hero">
    <div class="hero-content">
        <h2>Ben <span>Samet Çetinkuş</span><br>Siber Güvenlik Uzmanı & Yazılımcı</h2>
        <p>
            6+ yıllık deneyimle siber güvenlik ve yazılım alanında aktif olarak çalışıyorum.
            Güvenli, ölçeklenebilir ve sürdürülebilir sistemler geliştiriyorum.
        </p>
        <a href="#hakkimda" class="btn">Daha Fazla</a>
    </div>
</div>

<section id="hakkimda">
    <h2>Hakkımda</h2>
    <div class="card">
        👋 Merhaba, ben Samet Çetinkuş.<br><br>

        Yaklaşık 6 yıldır bilişim teknolojileri alanında aktif olarak projeler geliştiriyorum.
        Bu süreçte hem pratik hem teorik olarak kendimi geliştirerek siber güvenlik ve yazılım alanında uzmanlaştım.<br><br>

        Sistemlerdeki zafiyetleri analiz etmek, tehditleri tespit etmek ve çözüm üretmek üzerine çalışıyorum.<br><br>

        Nexora Siber Güvenlik ve Yazılım firmasının kurucusu olarak,
        teknik bilgi ve tecrübemi gerçek dünya projelerine dönüştürüyorum.
    </div>
</section>

<section id="yetenek">
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

<section>
    <h2>Uzmanlık Alanları</h2>

    <div class="grid">
        <div class="card">Penetration Testing</div>
        <div class="card">Web Security</div>
        <div class="card">Network Security</div>
        <div class="card">Secure Coding</div>
    </div>
</section>

<section id="iletisim">
    <h2>İletişim</h2>
    <div class="card">
        Email: seninmailin@example.com
    </div>
</section>

<footer>
    © 2026 Samet Çetinkuş
</footer>

</body>
</html>
