<!DOCTYPE html>
<html lang="my">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Win Lwin Tun | Pro Max Studio</title>

<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css">
<link href="https://fonts.googleapis.com/css2?family=Cinzel:wght@400;600;800&display=swap" rel="stylesheet">

<style>

body{
    margin:0;
    font-family:Arial;
    background:linear-gradient(135deg,#0f172a,#111827);
    color:Green;
}

/* HEADER */
header{
    text-align:center;
    padding:15px;
    background:rgba(0,0,0,0.4);
    backdrop-filter:blur(10px);
}

/* LOGO IMAGE */
.logo{
    width:90px;
    height:90px;
    border-radius:50%;
    object-fit:cover;
    border:2px solid #d4af37;
}

logo-wrapper {
    text-align:center;
    display:flex;
    flex-direction:column;
    align-items:center;
    gap:10px;
}

.logo-circle {
    width:80px;
    height:80px;
    border-radius:50%;
    border:2px solid #d4af37;
    display:flex;
    justify-content:center;
    align-items:center;
    position:relative;
    background: radial-gradient(circle, #1a1a1a 0%, #0b0c10 100%);
}

.logo-circle::after {
    content:'';
    position:absolute;
    width:88px;
    height:88px;
    border-radius:50%;
    border:1px dashed rgba(212,175,55,0.4);
}

.logo-w {
    font-family:'Cinzel', serif;
    font-size:3rem;
    font-weight:800;
    background: linear-gradient(135deg, #f3e5ab 0%, #d4af37 50%, #aa7c11 100%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    text-shadow:0px 4px 10px rgba(0,0,0,0.5);
}

.logo-text {
    font-family:'Cinzel', serif;
    font-size:1.2rem;
    font-weight:600;
    letter-spacing:4px;
    background: linear-gradient(to right, #ffffff 60%, #d4af37);
    -webkit-background-clip:text;
    -webkit-text-fill-color:transparent;
}

section {
    padding:60px 20px;
    max-width:1000px;
    margin:auto;
}

h1,h2 {
    color:#1E88E5;
    text-align:center;
}

/* FIXED P TAG */
p {
    text-align:center;
    margin-bottom:20px;
}

/* HERO */
.hero{
    text-align:center;
    padding:60px 20px;
}

/* CARD */
.card{
    background:rgba(255,255,255,0.06);
    margin:20px auto;
    width:90%;
    max-width:420px;
    padding:20px;
    border-radius:15px;
    backdrop-filter:blur(10px);
    border:1px solid rgba(255,255,255,0.1);
}

/* BUTTON */
.btn{
    display:flex;
    align-items:center;
    justify-content:center;
    gap:10px;
    padding:12px;
    margin:10px auto;
    width:240px;
    border-radius:12px;
    background:rgba(255,255,255,0.08);
    color:white;
    text-decoration:none;
    transition:.2s;
}

.btn:active{
    transform:scale(0.95);
}

/* CHAT BUTTON */
.chat-btn{
    position:fixed;
    bottom:20px;
    right:20px;
    background:#38bdf8;
    color:black;
    padding:15px;
    border-radius:50%;
    cursor:pointer;
    font-size:18px;
}

/* CHAT BOX */
#chatBox{
    position:fixed;
    bottom:80px;
    right:20px;
    width:300px;
    height:420px;
    background:#0f172a;
    border:1px solid #38bdf8;
    border-radius:12px;
    display:none;
    flex-direction:column;
}

.chat-header{
    background:#38bdf8;
    color:black;
    padding:10px;
    display:flex;
    justify-content:space-between;
}

#messages{
    flex:1;
    padding:10px;
    overflow:auto;
    font-size:14px;
}

.chat-input{
    display:flex;
    border-top:1px solid #333;
}

.chat-input input{
    flex:1;
    padding:10px;
    border:none;
    outline:none;
}

.chat-input button{
    background:#38bdf8;
    border:none;
    padding:10px;
}

</style>
</head>

<body>

<header>
    <img class="logo" src="1000022537.png" alt="logo">
    <h3>Win Lwin Tun</h3>
</header>

<section class="hero">
    <h1>Pro Max Web Developer</h1>
    <p>Modern • Clean • Creative • Fast</p>
</section>

<div class="card">

    <h3>Contact Me</h3>

    <a class="btn" href="tel:0824542317">
        📞 0824542317
    </a>

    <a class="btn" href="https://www.facebook.com/share/1FxH3BP9ti/" target="_blank">
        <i class="fab fa-facebook"></i> Facebook Profile
    </a>

    <a class="btn" href="https://t.me/winlwin1500" target="_blank">
        <i class="fab fa-telegram"></i> Telegram @winlwin1500
    </a>

    <div class="btn">
        ✉ WINLWINTUN.CK2@gmail.com
    </div>

</div>

<div class="chat-btn" onclick="toggleChat()">💬</div>

<div id="chatBox">

    <div class="chat-header">
        Chat Developer
        <span onclick="toggleChat()" style="cursor:pointer;">✖</span>
    </div>

    <div id="messages"></div>

    <div class="chat-input">
        <input id="input" placeholder="Type message...">
        <button onclick="sendMsg()">Send</button>
    </div>

</div>

<script>

function toggleChat(){
    let box=document.getElementById("chatBox");
    box.style.display = (box.style.display==="flex") ? "none" : "flex";
}

function sendMsg(){
    let input=document.getElementById("input");
    let msg=input.value;
    if(!msg) return;

    let box=document.getElementById("messages");

    box.innerHTML += "<div>👤 You: " + msg + "</div>";

    setTimeout(()=>{
        box.innerHTML += "<div>👨‍💻 Dev: ငါကဝင်းလွင်ထွန်းပါ ဘာကူညီရမလဲ 😎</div>";
        box.scrollTop = box.scrollHeight;
    },500);

    input.value="";
}

</script>

</body>
</html>
