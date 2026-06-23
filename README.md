l>
<html>lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>W. SANTOS - Salgados</title>

<style>
*{
margin:0;
padding:0;
box-sizing:border-box;
font-family:Arial,sans-serif;
}

body{
background:linear-gradient(-45deg,#ff9800,#ff5722,#ffc107,#ff7043);
background-size:400% 400%;
animation:fundo 10s ease infinite;
padding:20px;
}

@keyframes fundo{
0%{background-position:0% 50%;}
50%{background-position:100% 50%;}
100%{background-position:0% 50%;}
}

header{
text-align:center;
color:white;
margin-bottom:25px;
}

header h1{
font-size:42px;
text-shadow:2px 2px 8px rgba(0,0,0,.3);
}

header p{
font-size:18px;
}

.produtos{
display:grid;
grid-template-columns:repeat(auto-fit,minmax(300px,1fr));
gap:20px;
}

.card{
background:#fff;
border-radius:20px;
overflow:hidden;
box-shadow:0 5px 15px rgba(0,0,0,.2);
transition:.3s;
}

.card:hover{
transform:translateY(-8px);
}

.card img{
width:100%;
height:220px;
object-fit:cover;
}

.info{
padding:15px;
}

.info h2{
color:#ff5722;
margin-bottom:10px;
}

.info p{
margin-bottom:5px;
}

select,input{
width:100%;
padding:10px;
margin-top:10px;
border:1px solid #ddd;
border-radius:10px;
}

button{
width:100%;
padding:12px;
margin-top:10px;
border:none;
border-radius:30px;
background:#25D366;
color:white;
font-size:16px;
cursor:pointer;
transition:.3s;
}

button:hover{
background:#1da851;
}

.carrinho{
background:white;
padding:20px;
margin-top:25px;
border-radius:20px;
box-shadow:0 5px 15px rgba(0,0,0,.2);
}

.carrinho h2{
color:#ff5722;
margin-bottom:10px;
}

#lista li{
margin:8px 0;
}

#total{
font-size:22px;
font-weight:bold;
margin-top:10px;
color:#ff5722;
}
</style>
</head>

<body>

<header>
<h1>🌟 W. SANTOS 🌟</h1>
<p>Qualidade e sabor em cada mordida!</p>
</header>

<div class="produtos">

<!-- BOLINHO -->
<div class="card">
<img src="1782217178021.jpeg" alt="Bolinho de Queijo">

<div class="info">
<h2>🥟 Bolinho de Queijo</h2>

<p>1 unidade - R$ 3,50</p>
<p>3 unidades - R$ 10,00</p>

<select id="bolinhoTipo">
<option value="3.5">1 Unidade</option>
<option value="10">3 Unidades</option>
</select>

<input type="number" id="qtdBolinho" min="1" value="1">

<button onclick="adicionar('Bolinho de Queijo',bolinhoTipo.value,qtdBolinho.value)">
Adicionar
</button>
</div>
</div>

<!-- COXINHA -->
<div class="card">
  
</a>
<div class="info">
<h2>🍗 Coxinha</h2>

<p>1 unidade - R$ 3,50</p>
<p>3 unidades - R$ 10,00</p>

<select id="coxinhaTipo">
<option value="3.5">1 Unidade</option>
<option value="10">3 Unidades</option>
</select>

<input type="number" id="qtdCoxinha" min="1" value="1">

<button onclick="adicionar('Coxinha',coxinhaTipo.value,qtdCoxinha.value)">
Adicionar
</button>
</div>
</div>

<!-- SALSICHÃO -->
<div class="card">
<img src="1782217185142.jpeg" alt="Salsichão">

<div class="info">
<h2>🌭 Salsichão</h2>

<p>1 unidade - R$ 3,50</p>
<p>3 unidades - R$ 10,00</p>

<select id="salsichaoTipo">
<option value="3.5">1 Unidade</option>
<option value="10">3 Unidades</option>
</select>

<input type="number" id="qtdSalsichao" min="1" value="1">

<button onclick="adicionar('Salsichão',salsichaoTipo.value,qtdSalsichao.value)">
Adicionar
</button>
</div>
</div>

<!-- MINI SALGADOS -->
<div class="card">
<img src="1782217187606.jpeg" alt="Mini Salgados">

<div class="info">
<h2>🎉 Mini Salgados</h2>

<select id="miniTipo">
<option>Mini Coxinha</option>
<option>Mini Bolinha de Queijo</option>
<option>Mini Salsichão</option>
<option>Mini Enroladinho</option>
</select>

<p>R$ 0,50 por unidade</p>

<input type="number" id="qtdMini" min="1" value="1">

<button onclick="adicionarMini()">
Adicionar
</button>
</div>
</div>

<!-- PASTEL -->
<div class="card">
<img src="1782217190007.jpeg" alt="Pastel">

<div class="info">
<h2>🥙 Pastel</h2>

<select id="tipoPastel">
<option value="5">1 Sabor - R$ 5,00</option>
<option value="7">2 Sabores - R$ 7,00</option>
<option value="15">3 Sabores ou Mais - R$ 15,00</option>
</select>

<select id="sabor1">
<option>Carne</option>
<option>Frango</option>
<option>Queijo</option>
<option>Calabresa</option>
<option>Pizza</option>
<option>Carne de Sol</option>
<option>Frango com Catupiry</option>
<option>Presunto e Queijo</option>
<option>Bacon com Queijo</option>
<option>Camarão</option>
<option>Chocolate</option>
<option>Banana com Canela</option>
</select>

<select id="sabor2">
<option>Nenhum</option>
<option>Carne</option>
<option>Frango</option>
<option>Queijo</option>
<option>Calabresa</option>
<option>Pizza</option>
</select>

<select id="sabor3">
<option>Nenhum</option>
<option>Carne</option>
<option>Frango</option>
<option>Queijo</option>
<option>Calabresa</option>
<option>Pizza</option>
</select>

<input type="number" id="qtdPastel" min="1" value="1">

<button onclick="adicionarPastel()">
Adicionar
</button>

</div>
</div>

</div>

<div class="carrinho">

<h2>🛒 Carrinho</h2>

<ul id="lista"></ul>

<div id="total">
Total: R$ 0,00
</div>

<button onclick="enviarWhatsApp()">
📲 Finalizar Pedido
</button>

</div>

<script>

let carrinho = [];
let total = 0;

function atualizar(){

let lista = document.getElementById("lista");
lista.innerHTML = "";

carrinho.forEach((item,index)=>{

lista.innerHTML += `
<li>
${item.nome}
<button onclick="remover(${index})">❌</button>
</li>
`;

});

document.getElementById("total").innerHTML =
"Total: R$ " + total.toFixed(2);

}

function adicionar(nome,preco,qtd){

preco = Number(preco);
qtd = Number(qtd);

carrinho.push({
nome:`${qtd}x ${nome}`,
preco:preco*qtd
});

total += preco*qtd;

atualizar();
}

function adicionarMini(){

let tipo = document.getElementById("miniTipo").value;
let qtd = Number(document.getElementById("qtdMini").value);

carrinho.push({
nome:`${qtd}x ${tipo}`,
preco:qtd*0.5
});

total += qtd*0.5;

atualizar();
}

function adicionarPastel(){

let preco = Number(document.getElementById("tipoPastel").value);
let qtd = Number(document.getElementById("qtdPastel").value);

let s1 = document.getElementById("sabor1").value;
let s2 = document.getElementById("sabor2").value;
let s3 = document.getElementById("sabor3").value;

let sabores = [s1];

if(s2!="Nenhum") sabores.push(s2);
if(s3!="Nenhum") sabores.push(s3);

carrinho.push({
nome:`${qtd}x Pastel (${sabores.join(", ")})`,
preco:preco*qtd
});

total += preco*qtd;

atualizar();
}

function remover(index){

total -= carrinho[index].preco;
carrinho.splice(index,1);

atualizar();
}

function enviarWhatsApp(){

let msg = "Olá, gostaria de fazer o pedido:%0A%0A";

carrinho.forEach(item=>{
msg += "• " + item.nome + "%0A";
});

msg += "%0A💰 Total: R$ " + total.toFixed(2);

window.open(
"https://wa.me/5589981032073?text="+msg,
"_blank"
);

}

</script>

</body>
</html>
