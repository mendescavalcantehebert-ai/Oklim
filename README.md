<!DOCTYPE html>
<html lang="pt-br">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Oklim - Óculos de Sol</title>
<style>
body{
    font-family: Arial;
    margin:0;
    background:#f5f5f5;
}
header{
    background:black;
    color:white;
    padding:20px;
    text-align:center;
}
.produtos{
    display:flex;
    flex-wrap:wrap;
    justify-content:center;
    padding:20px;
}
.produto{
    background:white;
    width:200px;
    margin:10px;
    padding:15px;
    border-radius:10px;
    box-shadow:0 0 10px rgba(0,0,0,0.1);
    text-align:center;
}
button{
    background:gold;
    border:none;
    padding:10px;
    border-radius:5px;
    cursor:pointer;
}
button:hover{
    background:orange;
}
.carrinho{
    position:fixed;
    bottom:0;
    width:100%;
    background:black;
    color:white;
    padding:15px;
    text-align:center;
}
</style>
</head>
<body>

<header>
<h1>OKLIM 👓</h1>
<p>Óculos de Sol Premium</p>
</header>

<div class="produtos">

<div class="produto">
<h3>Modelo 01</h3>
<p>R$ 29,99</p>
<button onclick="addCarrinho()">Adicionar</button>
</div>

<div class="produto">
<h3>Modelo 02</h3>
<p>R$ 29,99</p>
<button onclick="addCarrinho()">Adicionar</button>
</div>

<div class="produto">
<h3>Modelo 03</h3>
<p>R$ 29,99</p>
<button onclick="addCarrinho()">Adicionar</button>
</div>

</div>

<div class="carrinho">
<span id="total">Total: R$ 0,00</span>
<br><br>
<a href="https://wa.me/5581989716681" target="_blank">
<button>Finalizar pelo WhatsApp</button>
</a>
</div>

<script>
let total = 0;

function addCarrinho(){
    total += 29.99;
    document.getElementById("total").innerHTML = 
    "Total: R$ " + total.toFixed(2).replace(".", ",");
}
</script>

</body>
</html>
