<!DOCTYPE html>
<html lang="my">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Win Lwin Tun | Pro Max Studio</title>

<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css">

<style>

/* ================= LOADING လိုင်းကျတာနေမှာ မြန်မာနိုင်ငံကပဲနေမယ်😝================= */
#loading{
    position:fixed;
    top:0;
    left:0;
    width:100%;
    height:100%;
    background:#0f172a;
    display:flex;
    flex-direction:column;
    justify-content:center;
    align-items:center;
    color:white;
    z-index:999999;
}

.spinner{
    width:50px;
    height:50px;
    border:5px solid #333;
    border-top:5px solid #38bdf8;
    border-radius:50%;
    animation:spin 1s linear infinite;
}

@keyframes spin{
    0%{transform:rotate(0deg);}
    100%{transform:rotate(360deg);}
}

/* ================= INTRO ================= */
#intro{
    position:fixed;
    top:0;
    left:0;
    width:100%;
    height:100%;
    background:#0f172a;
    display:flex;
    justify-content:center;
    align-items:center;
    flex-direction:column;
    z-index:999998;
    animation:fadeOut 1.8s ease forwards;
    animation-delay:2.5s;
}

@keyframes fadeOut{
    to{
        opacity:0;
        visibility:hidden;
    }
}

/* ================= TEXT ================= */
.intro-content h1{
    font-size:3rem;
    color:#38bdf8;
    font-weight:800;
    animation:float3d 3s ease-in-out infinite, neon 2s infinite;
    text-shadow:0 0 10px #38bdf8;
}

@keyframes float3d{
    0%{transform:translateY(0);}
    50%{transform:translateY(-10px);}
    100%{transform:translateY(0);}
}

@keyframes neon{
    0%{color:#38bdf8;}
    25%{color:#f472b6;}
    50%{color:#facc15;}
    75%{color:#34d399;}
    100%{color:#38bdf8;}
}

/* ================= TYPING ================= */
#typing-text{
    margin-top:10px;
    font-size:1.2rem;
    color:white;
}

#typing-text::after{
    content:"|";
    animation:blink 0.7s infinite;
}

@keyframes blink{
    50%{opacity:0;}
}

/* ================= MAIN ================= */
body{
    margin:0;
    font-family:Arial;
    background:linear-gradient(135deg,#0f172a,#111827);
    color:white;
}

header{
    text-align:center;
    padding:15px;
}

.logo{
    width:90px;
    height:90px;
    border-radius:50%;
    border:2px solid #d4af37;
}

.hero{
    text-align:center;
    padding:40px 20px;
}

.card{
    background:rgba(255,255,255,0.06);
    margin:20px auto;
    width:90%;
    max-width:420px;
    padding:20px;
    border-radius:15px;
}

/* BUTTON */
.btn{
    display:flex;
    justify-content:center;
    align-items:center;
    padding:12px;
    margin:10px auto;
    width:240px;
    border-radius:12px;
    background:rgba(255,255,255,0.08);
    color:white;
    text-decoration:none;
}

/* CHAT */
.chat-btn{
    position:fixed;
    bottom:20px;
    right:20px;
    background:#38bdf8;
    padding:15px;
    border-radius:50%;
}

#chatBox{
    position:fixed;
    bottom:80px;
    right:20px;
    width:300px;
    height:420px;
    background:#0f172a;
    display:none;
    flex-direction:column;
    border:1px solid #38bdf8;
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
}

.chat-input{
    display:flex;
}

.chat-input input{
    flex:1;
    padding:10px;
}

.chat-input button{
    padding:10px;
    background:#38bdf8;
    border:none;
}

</style>
</head>

<body>

<!-- LOADING -->
<div id="loading">
    <div class="spinner"></div>
    <p>Loading...</p>
</div>

<!-- INTRO -->
<div id="intro">
    <div class="intro-content">
        <h1>Win Lwin Tun</h1>
        <div id="typing-text"></div>
    </div>
</div>

<header>
    <img class="logo" src="1000022537.png" alt="">
    <h3>Win Lwin Tun</h3>
</header>

<div class="hero">
    <h1>Pro Max Developer</h1>
    <p>Modern • Clean • Creative</p>
</div>

<div class="card">
    <a class="btn" href="tel:0824542317">📞 Call</a>
    <a class="btn" href="https://facebook.com" target="_blank">Facebook</a>
    <a class="btn" href="https://t.me" target="_blank">Telegram</a>
</div>

<div class="chat-btn" onclick="toggleChat()">💬</div>

<div id="chatBox">
    <div class="chat-header">
        Chat
        <span onclick="toggleChat()">✖</span>
    </div>
    <div id="messages"></div>
    <div class="chat-input">
        <input id="input">
        <button onclick="sendMsg()">Send</button>
    </div>
</div>

<script>

/* LOADING SAFE REMOVE */
window.addEventListener("load",()=>{
    setTimeout(()=>{
        document.getElementById("loading").style.display="none";
    },500);
});

/* INTRO AUTO REMOVE */
setTimeout(()=>{
    let intro=document.getElementById("intro");
    if(intro) intro.remove();
},3000);

/* TYPING EFFECT */
const texts=[
"Loading Pro System...",
"Initializing UI...",
"Welcome to Win Lwin Tun 🚀",
"Modern • Clean • Pro Max"
];

let i=0,j=0,del=false;

function type(){
    let el=document.getElementById("typing-text");
    if(!el) return;

    let word=texts[i];

    el.innerHTML=word.substring(0,j);

    if(!del){
        j++;
        if(j>word.length){del=true;setTimeout(type,1000);return;}
    }else{
        j--;
        if(j===0){del=false;i=(i+1)%texts.length;}
    }

    setTimeout(type,80);
}

window.addEventListener("load",()=>{
    setTimeout(type,800);
});

/* CHAT */
function toggleChat(){
    let box=document.getElementById("chatBox");
    box.style.display = box.style.display==="flex"?"none":"flex";
}

function sendMsg(){
    let input=document.getElementById("input");
    let msg=input.value;
    if(!msg) return;

    document.getElementById("messages").innerHTML += "👤 "+msg+"<br>";

    setTimeout(()=>{
        document.getElementById("messages").innerHTML += "👨‍💻 Dev reply<br>";
    },500);

    input.value="";
}

</script>

</body>
</html>
