<!DOCTYPE html>
<html lang="my">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Win Lwin Tun - Web Developer</title>
<style>
@import url('https://fonts.googleapis.com/css2?family=Cinzel:wght@600;800&display=swap');
body { margin:0; font-family:'Segoe UI', Tahoma, Geneva, Verdana, sans-serif; background:#f0f2f5; color:#333; }
header { background:#0b0c10; color:white; padding:20px 0; text-align:center; position:sticky; top:0; z-index:1000; }
header nav a { color:white; text-decoration:none; margin:0 15px; font-weight:bold; }
header nav a:hover { text-decoration:underline; }
.logo-wrapper { text-align:center; display:flex; flex-direction:column; align-items:center; gap:10px; }
.logo-circle { width:80px; height:80px; border-radius:50%; border:2px solid #d4af37; display:flex; justify-content:center; align-items:center; position:relative; background: radial-gradient(circle, #1a1a1a 0%, #0b0c10 100%); }
.logo-circle::after { content:''; position:absolute; width:88px; height:88px; border-radius:50%; border:1px dashed rgba(212,175,55,0.4); }
.logo-w { font-family:'Cinzel', serif; font-size:3rem; font-weight:800; background: linear-gradient(135deg, #f3e5ab 0%, #d4af37 50%, #aa7c11 100%); -webkit-background-clip: text; -webkit-text-fill-color: transparent; text-shadow:0px 4px 10px rgba(0,0,0,0.5); }
.logo-text { font-family:'Cinzel', serif; font-size:1.2rem; font-weight:600; letter-spacing:4px; background: linear-gradient(to right, #ffffff 60%, #d4af37); -webkit-background-clip:text; -webkit-text-fill-color:transparent; }
section { padding:60px 20px; max-width:1000px; margin:auto; }
h1,h2 { color:#1E88E5; text-align:center; }
p { text-align:center; margin-bottom:20px; }
.hero { display:flex; flex-direction:column; align-items:center; justify-content:center; text-align:center; gap:10px; }
.services, .portfolio { display:grid; grid-template-columns:repeat(auto-fit, minmax(220px,1fr)); gap:20px; }
.card { background:white; padding:20px; border-radius:8px; box-shadow:0 2px 8px rgba(0,0,0,0.1); text-align:center; }
.contact-form { display:flex; flex-direction:column; gap:15px; max-width:500px; margin:auto; }
input, textarea { padding:10px; border:1px solid #ccc; border-radius:5px; }
button { padding:12px; background:#1E88E5; color:white; border:none; border-radius:5px; cursor:pointer; }
button:hover { background:#1565C0; }
footer { text-align:center; padding:20px 0; background:#333; color:white; margin-top:40px; }
@media(max-width:600px){ header nav { display:flex; flex-direction:column; gap:10px; } }
</style>
</head>
<body>

<header>
    <!-- Logo HTML -->
    <div class="logo-wrapper">
        <div class="logo-circle"><h1 class="logo-w">W</h1></div>
        <h2 class="logo-text">Winlwintun</h2>
    </div>
    <!-- Navigation -->
    <nav>
        <a href="#hero">Home</a>
        <a href="#about">About</a>
        <a href="#services">Services</a>
        <a href="#portfolio">Projects</a>
        <a href="#contact">Contact</a>
    </nav>
</header>

<section id="hero" class="hero">
    <h1>Win Lwin Tun</h1>
    <p>Web Developer | Modern, Responsive Websites</p>
</section>

<section id="about">
    <h2>About Me</h2>
    <p>I am a passionate web developer building clean, responsive, and user-friendly websites. I love turning ideas into real web solutions.</p>
</section>

<section id="services">
    <h2>Services</h2>
    <div class="services">
        <div class="card"><h3>Web Design</h3><p>Modern, clean and user-friendly websites.</p></div>
        <div class="card"><h3>Web Development</h3><p>Responsive websites using modern technologies.</p></div>
        <div class="card"><h3>Responsive Design</h3><p>Looks great on all devices.</p></div>
        <div class="card"><h3>SEO Friendly</h3><p>Optimized for search engines.</p></div>
    </div>
</section>

<section id="portfolio">
    <h2>Portfolio</h2>
    <div class="portfolio">
        <div class="card"><h3>Project 1</h3><p>Landing page</p></div>
        <div class="card"><h3>Project 2</h3><p>Portfolio showcase</p></div>
        <div class="card"><h3>Project 3</h3><p>Blog page</p></div>
    </div>
</section>

<section id="contact">
    <h2>Contact Me</h2>
    <div class="logo-wrapper" style="margin-bottom:20px;">
        <div class="logo-circle"><h1 class="logo-w">W</h1></div>
        <h2 class="logo-text">Winlwintun</h2>
    </div>
    <form action="mailto:WINLWINTUN.CK2@gmail.com" method="post" enctype="text/plain" class="contact-form">
        <input type="text" name="name" placeholder="နာမည်" required>
        <input type="email" name="email" placeholder="Email" required>
        <textarea name="message" placeholder="Message" rows="5" required></textarea>
        <button type="submit">Send Message</button>
    </form>
    <p style="color:#555;">သင့် message ကို သင့် Gmail သို့ ပို့မည်</p>
    <div style="text-align:center; margin-top:20px; font-size:16px;">
        <p>📞 Phone: 0824542317</p>
        <p>🌐 Facebook: <a href="https://www.facebook.com/share/1FxH3BP9ti/" target="_blank" style="color:#1E88E5;">https://www.facebook.com/share/1FxH3BP9ti/</a></p>
        <p>✉ Email: WINLWINTUN.CK2@gmail.com</p>
        <p>💬 Chat with me: <a href="https://chatgpt.com/s/m_6a2c049fccdc819182ebda2309c9fda8" target="_blank" style="color:#1E88E5;">Chat Here</a></p>
    </div>
</section>

<footer>
    &copy; 2026 Win Lwin Tun. All rights reserved.
</footer>

</body>
</html>Encoding: UTF-8
