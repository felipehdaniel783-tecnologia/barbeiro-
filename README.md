<!DOCTYPE html>
<html lang="pt-br">

<head>

<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>BarberPro</title>

<style>

*{
    margin:0;
    padding:0;
    box-sizing:border-box;
    font-family:Arial;
}

body{
    background:#111;
    color:white;
}

/* TOPO */

header{

    background:#000;
    padding:20px;
    text-align:center;
    border-bottom:3px solid #d4af37;
}

header h1{

    color:#d4af37;
    font-size:35px;
}

/* BANNER */

.banner{

    height:300px;
    background:url('https://images.unsplash.com/photo-1517832606299-7ae9b720a186?q=80&w=1200&auto=format&fit=crop') center/cover;
    display:flex;
    justify-content:center;
    align-items:center;
}

.banner h2{

    background:rgba(0,0,0,0.7);
    padding:20px;
    border-radius:15px;
    font-size:35px;
}

/* CONTAINER */

.container{

    padding:20px;
}

/* CARDS */

.card{

    background:#1b1b1b;
    padding:20px;
    border-radius:20px;
    margin-bottom:20px;
    border:1px solid #333;
}

/* INPUTS */

input,
select{

    width:100%;
    padding:12px;
    margin-top:10px;
    border:none;
    border-radius:10px;
}

/* BOTÃO */

button{

    width:100%;
    padding:15px;
    margin-top:15px;
    border:none;
    border-radius:10px;
    background:#d4af37;
    color:black;
    font-size:18px;
    cursor:pointer;
    font-weight:bold;
}

/* SERVIÇOS */

.servicos{

    display:grid;
    grid-template-columns:repeat(auto-fit,minmax(200px,1fr));
    gap:15px;
}

.servico{

    background:#222;
    padding:20px;
    border-radius:15px;
    text-align:center;
}

/* FOOTER */

footer{

    background:#000;
    text-align:center;
    padding:20px;
    margin-top:20px;
}

/* MOBILE */

@media(max-width:700px){

.banner h2{

    font-size:25px;
    text-align:center;
}

}

</style>

</head>

<body>

<!-- TOPO -->

<header>

<h1>💈 BarberPro</h1>

<p>Agende seu corte online</p>

</header>

<!-- BANNER -->

<div class="banner">

<h2>
Seu estilo começa aqui ✂️
</h2>

</div>

<!-- CONTAINER -->

<div class="container">

<!-- SERVIÇOS -->

<div class="card">

<h2>🔥 Serviços</h2>

<br>

<div class="servicos">

<div class="servico">

<h3>Corte Degradê</h3>

<p>R$ 35</p>

</div>

<div class="servico">

<h3>Barba</h3>

<p>R$ 20</p>

</div>

<div class="servico">

<h3>Sobrancelha</h3>

<p>R$ 10</p>

</div>

<div class="servico">

<h3>Corte + Barba</h3>

<p>R$ 50</p>

</div>

</div>

</div>

<!-- AGENDAMENTO -->

<div class="card">

<h2>📅 Agendar Horário</h2>

<input type="text"
id="nome"
placeholder="Seu nome">

<input type="tel"
id="telefone"
placeholder="Seu telefone">

<select id="servico">

<option>
Escolha o serviço
</option>

<option>Corte Degradê</option>
<option>Barba</option>
<option>Sobrancelha</option>
<option>Corte + Barba</option>

</select>

<input type="date"
id="data">

<input type="time"
id="hora">

<button onclick="agendar()">

Agendar pelo WhatsApp

</button>

</div>

<!-- HORÁRIOS -->

<div class="card">

<h2>⏰ Horários de Funcionamento</h2>

<br>

<p>Segunda a Sexta: 09:00 às 20:00</p>

<p>Sábado: 09:00 às 18:00</p>

<p>Domingo: Fechado</p>

</div>

</div>

<!-- RODAPÉ -->

<footer>

© 2026 BarberPro - Todos os direitos reservados

</footer>

<script>

/* ================================= */
/* AGENDAMENTO WHATSAPP */
/* ================================= */

function agendar(){

let nome =
document.getElementById("nome").value;

let telefone =
document.getElementById("telefone").value;

let servico =
document.getElementById("servico").value;

let data =
document.getElementById("data").value;

let hora =
document.getElementById("hora").value;

/* SE CAMPOS VAZIOS */

if(nome == "" ||
telefone == "" ||
data == "" ||
hora == ""){

alert("Preencha todos os campos");

return;

}

/* NUMERO WHATSAPP */

/*
Troque pelo seu número
Exemplo:
5518999999999
*/

let numero =
"5518996593045";

/* MENSAGEM */

let mensagem =

`💈 NOVO AGENDAMENTO 💈

👤 Nome: ${nome}

📞 Telefone: ${telefone}

✂️ Serviço: ${servico}

📅 Data: ${data}

⏰ Hora: ${hora}`;

/* LINK WHATSAPP */

let link =

`https://wa.me/${numero}?text=${encodeURIComponent(mensagem)}`;

/* ABRIR WHATSAPP */

window.open(link, "_blank");

}

</script>

</body> 
</html>
