<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>macaw.bet - Copa do Mundo</title>
<script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
<style>
body{font-family:Arial,Helvetica,sans-serif;margin:0;background:#2e1065;color:white;overflow-x:hidden}

/* fundo com arara */
body::before{content:"";position:fixed;left:0;top:0;width:100%;height:100%;background:url("https://upload.wikimedia.org/wikipedia/commons/0/0f/Anodorhynchus_hyacinthinus_-Bonito%2C_Mato_Grosso_do_Sul%2C_Brazil-8.jpg") center/cover no-repeat;opacity:0.25;z-index:-1}

/* arara animada */
.arara{position:fixed;bottom:20px;left:-120px;font-size:60px;animation:voar 20s linear infinite}
@keyframes voar{0%{left:-120px}100%{left:110%}}

.overlay{background:rgba(46,16,101,0.9);min-height:100vh;padding:30px}

.container{max-width:1200px;margin:auto;background:#4c1d95;padding:25px;border-radius:16px;box-shadow:0 10px 25px rgba(0,0,0,0.5);margin-bottom:20px}

.brand{font-size:42px;font-weight:bold;text-align:center;margin-bottom:10px}

h1,h2,h3{text-align:center}

input,select{padding:8px;border-radius:8px;border:none;margin:5px}

button{padding:10px 18px;border:none;border-radius:10px;background:#c4b5fd;color:black;font-weight:bold;cursor:pointer}

.game{background:#6d28d9;padding:15px;border-radius:10px;margin-top:15px}

.hidden{display:none}

.notice{font-size:12px;text-align:center;margin-bottom:10px}

.group{margin-top:25px;background:#5b21b6;padding:15px;border-radius:12px}

table{width:100%;margin-top:10px;border-collapse:collapse}

td,th{padding:8px;background:#7c3aed;border-bottom:1px solid #5b21b6;text-align:center}

.footer{text-align:center;font-size:12px;margin-top:20px;opacity:0.8}
</style>
</head>
<body>

<div class="arara">🦜</div>

<div class="overlay">

<div class="container" id="loginBox">

<div class="brand">macaw.bet</div>

<p class="notice">Simulador educativo de apostas da Copa do Mundo (sem dinheiro real)</p>

<select id="tipoLogin">
<option value="aluno">Aluno</option>
<option value="professor">Professor</option>
</select><br>

<input type="text" id="nome" placeholder="Nome"><br>
<input type="text" id="turma" placeholder="Turma"><br>
<input type="email" id="email" placeholder="Email institucional"><br>
<input type="password" id="senha" placeholder="Senha"><br>

<button onclick="login()">Entrar</button>

<p id="loginMsg"></p>

</div>

<div class="container hidden" id="site">
<h1>Palpites da Copa ⚽</h1>
<div id="jogos"></div>
</div>

<div class="container hidden" id="rankingBox">
<h2>Ranking Geral 🏆</h2>
<table>
<thead>
<tr>
<th>Posição</th>
<th>Aluno</th>
<th>Turma</th>
<th>Pontos</th>
</tr>
</thead>
<tbody id="rankingTabela"></tbody>
</table>
</div>

<div class="container hidden" id="graficoBox">
<h2>Desempenho dos Alunos 📊</h2>
<canvas id="grafico"></canvas>
</div>

<div class="container hidden" id="professorBox">
<h2>Painel do Professor 👨‍🏫</h2>
<button onclick="mostrarRanking()">Atualizar ranking</button>
</div>

<div class="footer">Projeto criado por <b>Jesus Capobianco</b> | Instagram: @08_.jesus</div>

</div>

<script>

/* grupos da copa */

const grupos={
"Grupo A":["🇧🇷 Brasil vs 🇨🇭 Suíça","🇧🇷 Brasil vs 🇷🇸 Sérvia","🇨🇭 Suíça vs 🇷🇸 Sérvia"],
"Grupo B":["🏴 Inglaterra vs 🇺🇸 EUA","🏴 Inglaterra vs 🇮🇷 Irã","🇺🇸 EUA vs 🇮🇷 Irã"],
"Grupo C":["🇦🇷 Argentina vs 🇲🇽 México","🇦🇷 Argentina vs 🇵🇱 Polônia","🇲🇽 México vs 🇵🇱 Polônia"],
"Grupo D":["🇫🇷 França vs 🇩🇰 Dinamarca","🇫🇷 França vs 🇹🇳 Tunísia","🇩🇰 Dinamarca vs 🇹🇳 Tunísia"],
"Grupo E":["🇪🇸 Espanha vs 🇩🇪 Alemanha","🇪🇸 Espanha vs 🇯🇵 Japão","🇩🇪 Alemanha vs 🇯🇵 Japão"],
"Grupo F":["🇧🇪 Bélgica vs 🇭🇷 Croácia","🇧🇪 Bélgica vs 🇲🇦 Marrocos","🇭🇷 Croácia vs 🇲🇦 Marrocos"],
"Grupo G":["🇧🇷 Brasil vs 🇨🇲 Camarões","🇧🇷 Brasil vs 🇨🇭 Suíça","🇨🇲 Camarões vs 🇨🇭 Suíça"],
"Grupo H":["🇵🇹 Portugal vs 🇺🇾 Uruguai","🇵🇹 Portugal vs 🇰🇷 Coreia","🇺🇾 Uruguai vs 🇰🇷 Coreia"]
}

let usuario=null
let turmaUsuario=null

function criarJogos(){

let area=document.getElementById("jogos")
area.innerHTML=""

for(const grupo in grupos){

let bloco=document.createElement("div")
bloco.className="group"

bloco.innerHTML=`<h2>${grupo}</h2>`

area.appendChild(bloco)

grupos[grupo].forEach(jogo=>{

let div=document.createElement("div")
div.className="game"

div.innerHTML=`
<h3>${jogo}</h3>

<label>Vencedor</label><br>
<select class="vencedor">
<option>Time 1</option>
<option>Time 2</option>
<option>Empate</option>
</select><br>

<label>Placar</label><br>
<input type="number" class="g1" min="0" placeholder="Gols 1">
<input type="number" class="g2" min="0" placeholder="Gols 2"><br>

<label>Melhor jogador</label><br>
<input type="text" class="jogador"><br>

<button onclick="apostar(this)">Registrar palpite</button>

<p class="resultado"></p>
`

bloco.appendChild(div)

})

}

}

function login(){

let nome=document.getElementById("nome").value
let turma=document.getElementById("turma").value
let email=document.getElementById("email").value

if(nome==""||email==""){
 document.getElementById("loginMsg").innerText="Preencha os campos"
 return
}

if(!email.endsWith("@edu.mt.gov.br")){
 document.getElementById("loginMsg").innerText="Use email institucional"
 return
}

usuario=nome

turmaUsuario=turma

if(!localStorage.getItem("ranking")){
 localStorage.setItem("ranking",JSON.stringify([]))
}

criarJogos()

document.getElementById("loginBox").classList.add("hidden")

document.getElementById("site").classList.remove("hidden")

document.getElementById("rankingBox").classList.remove("hidden")

document.getElementById("graficoBox").classList.remove("hidden")

document.getElementById("professorBox").classList.remove("hidden")

mostrarRanking()

}

function apostar(btn){

let card=btn.parentElement

let g1=card.querySelector(".g1").value
let g2=card.querySelector(".g2").value

if(g1==""||g2==""){
 card.querySelector(".resultado").innerText="Complete o palpite"
 return
}

let pontos=10

if(g1===g2) pontos=15

if(Math.random()>0.85) pontos=30

card.querySelector(".resultado").innerText="Palpite salvo +"+pontos+" pontos"

salvarPontuacao(pontos)

}

function salvarPontuacao(pontos){

let ranking=JSON.parse(localStorage.getItem("ranking"))

let aluno=ranking.find(a=>a.nome===usuario)

if(aluno){
 aluno.pontos+=pontos
}else{
 ranking.push({nome:usuario,turma:turmaUsuario,pontos:pontos})
}

localStorage.setItem("ranking",JSON.stringify(ranking))

mostrarRanking()

}

function mostrarRanking(){

let ranking=JSON.parse(localStorage.getItem("ranking"))

ranking.sort((a,b)=>b.pontos-a.pontos)

let tabela=document.getElementById("rankingTabela")

 tabela.innerHTML=""

let nomes=[]
let pontos=[]

ranking.forEach((aluno,i)=>{

let linha=`<tr>
<td>${i+1}</td>
<td>${aluno.nome}</td>
<td>${aluno.turma}</td>
<td>${aluno.pontos}</td>
</tr>`

 tabela.innerHTML+=linha

nomes.push(aluno.nome)

pontos.push(aluno.pontos)

})

criarGrafico(nomes,pontos)

}

function criarGrafico(nomes,pontos){

let ctx=document.getElementById("grafico")

new Chart(ctx,{type:"bar",data:{labels:nomes,datasets:[{label:"Pontos",data:pontos}]}})

}

</script>

</body>
</html>
