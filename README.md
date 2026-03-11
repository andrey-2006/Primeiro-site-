<!DOCTYPE html>
<html lang="pt">
<head>
<meta charset="UTF-8">
<title>Love Across The Universe</title>

<style>

body{
margin:0;
font-family:Arial;
background:black;
color:white;
overflow:hidden;
text-align:center;
}

/* GALAXIA */

.galaxy{
position:fixed;
width:100%;
height:100%;
background:radial-gradient(circle,#1b2735,#090a0f);
z-index:-2;
}

/* ESTRELAS */

.star{
position:absolute;
width:2px;
height:2px;
background:white;
animation:move linear infinite;
}

@keyframes move{
from{transform:translateY(-10vh);}
to{transform:translateY(110vh);}
}

/* ESTRELA CADENTE */

.shooting{
position:absolute;
width:3px;
height:3px;
background:white;
box-shadow:0 0 10px white;
animation:shoot 8s linear infinite;
}

@keyframes shoot{
0%{transform:translate(-10vw,-10vh);opacity:0;}
10%{opacity:1;}
100%{transform:translate(110vw,110vh);opacity:0;}
}

/* URSO */

.bear{
position:fixed;
bottom:10px;
left:-100px;
font-size:50px;
animation:walk 18s linear infinite;
}

@keyframes walk{
0%{left:-100px;}
100%{left:110vw;}
}

/* CAIXAS */

.box{
position:absolute;
top:50%;
left:50%;
transform:translate(-50%,-50%);
background:rgba(0,0,0,0.75);
padding:40px;
border-radius:15px;
width:380px;
}

/* BOTÕES */

button{
padding:10px 20px;
border:none;
border-radius:8px;
margin-top:15px;
cursor:pointer;
font-size:16px;
}

.sim{
background:white;
color:#ff4f7b;
}

.nao{
background:#333;
color:white;
}

</style>
</head>

<body>

<div class="galaxy"></div>
<div class="shooting"></div>
<div class="bear">🧸</div>

<!-- SENHA -->

<div class="box" id="senhaBox">

<h2>🔒 Área Secreta</h2>

<p>Digite a senha</p>

<input type="password" id="senha">

<br><br>

<button onclick="verificar()">Entrar</button>

</div>

<!-- TEXTO -->

<div class="box" id="textoBox" style="display:none;">

<h2>Love Across The Universe 💫</h2>

<p>
Entre bilhões de estrelas,<br>
entre bilhões de caminhos,<br>
meu destino sempre seria você.
</p>

<p>
Você é o meu universo inteiro.
</p>

<button onclick="proxima()">Continuar</button>

</div>

<!-- PERGUNTA -->

<div class="box" id="perguntaBox" style="display:none;">

<h2>Uma pergunta ❤️</h2>

<p>Você quer continuar sendo minha namorada?</p>

<button class="sim" onclick="responder('SIM ❤️')">Sim</button>

<button class="nao" onclick="responder('NÃO 😅')">Não</button>

</div>

<script>

/* ESTRELAS */

for(let i=0;i<150;i++){

let s=document.createElement("div");

s.className="star";

s.style.left=Math.random()*100+"vw";

s.style.top=Math.random()*100+"vh";

s.style.animationDuration=(5+Math.random()*10)+"s";

document.body.appendChild(s);

}

/* amor */

function verificar(){

let senha=document.getElement
