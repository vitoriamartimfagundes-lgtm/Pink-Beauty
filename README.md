# Pink-Beauty<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Pink Beauty Blog</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap" rel="stylesheet">
<link rel="stylesheet" href="style.css">
</head>
<body>

<header>
    <nav>
        <h1>Pink Beauty</h1>

        <ul>
            <li><a href="#">Início</a></li>
            <li><a href="#">Maquiagem</a></li>
            <li><a href="#">Skincare</a></li>
            <li><a href="#">Perfumes</a></li>
            <li><a href="#">Contato</a></li>
        </ul>

        <button id="tema">🌙</button>
    </nav>

    <section class="hero">
        <div class="texto">
            <h2>Descubra sua beleza todos os dias</h2>
            <p>Dicas, tendências e novidades do universo da maquiagem, skincare e perfumes.</p>
            <button>Explorar</button>
        </div>
    </section>
</header>

<main>

<section class="cards">

<div class="card">
<img src="https://images.unsplash.com/photo-1522335789203-aabd1fc54bc9?w=600" alt="">
<h3>Maquiagem Glow</h3>
<p>Aprenda a criar uma pele iluminada e natural com poucos produtos.</p>
</div>

<div class="card">
<img src="https://images.unsplash.com/photo-1512496015851-a90fb38ba796?w=600" alt="">
<h3>Skincare Diário</h3>
<p>Rotina simples para manter sua pele saudável e hidratada.</p>
</div>

<div class="card">
<img src="https://images.unsplash.com/photo-1596462502278-27bfdc403348?w=600" alt="">
<h3>Perfumes Femininos</h3>
<p>Conheça fragrâncias elegantes para todas as ocasiões.</p>
</div>

</section>

<section class="newsletter">
<h2>veja novas novidades</h2>
<p>Cadastre seu e-mail para acompanhar tendências e promoções.</p>

<div class="form">
<input type="email" placeholder="Digite seu e-mail">
<button>Inscrever-se</button>
</div>

</section>

</main>

<footer>
<p>© 2026 Pink Beauty Blog • Todos os direitos reservados.</p>
</footer>

<script src="script.js"></script>
</body>
</html>*{
margin:0;
padding:0;
box-sizing:border-box;
font-family:Poppins,sans-serif;
}

body{
background:#fff5f9;
color:#444;
transition:.4s;
}

header{
background:linear-gradient(135deg,#ff6fa9,#ffb6d9);
color:white;
padding-bottom:60px;
}

nav{
display:flex;
justify-content:space-between;
align-items:center;
padding:20px 10%;
}

nav h1{
font-size:30px;
}

nav ul{
display:flex;
list-style:none;
gap:30px;
}

nav a{
text-decoration:none;
color:white;
font-weight:500;
}

nav button{
background:white;
color:#ff4f94;
border:none;
padding:10px 15px;
border-radius:50%;
cursor:pointer;
font-size:18px;
}

.hero{
display:flex;
justify-content:center;
align-items:center;
height:60vh;
text-align:center;
padding:20px;
}

.hero h2{
font-size:52px;
margin-bottom:20px;
}

.hero p{
font-size:18px;
max-width:650px;
margin:auto;
margin-bottom:30px;
}

.hero button{
padding:15px 35px;
border:none;
border-radius:30px;
background:white;
color:#ff4f94;
font-size:18px;
cursor:pointer;
transition:.3s;
}

.hero button:hover{
transform:scale(1.05);
}

.cards{
display:grid;
grid-template-columns:repeat(auto-fit,minmax(280px,1fr));
gap:30px;
padding:70px 10%;
}

.card{
background:white;
border-radius:20px;
overflow:hidden;
box-shadow:0 15px 30px rgba(0,0,0,.1);
transition:.4s;
}

.card:hover{
transform:translateY(-10px);
}

.card img{
width:100%;
height:220px;
object-fit:cover;
}

.card h3{
padding:20px;
color:#ff4f94;
}

.card p{
padding:0 20px 30px;
}

.newsletter{
background:#ffd6e8;
text-align:center;
padding:70px 20px;
}

.newsletter h2{
font-size:38px;
color:#ff2f7d;
}

.newsletter p{
margin:20px 0;
}

.form{
display:flex;
justify-content:center;
gap:10px;
flex-wrap:wrap;
}

.form input{
padding:15px;
width:320px;
border:none;
border-radius:30px;
}

.form button{
padding:15px 30px;
background:#ff4f94;
color:white;
border:none;
border-radius:30px;
cursor:pointer;
}

footer{
background:#ff4f94;
padding:25px;
color:white;
text-align:center;
}

.dark{
background:#24131a;
color:white;
}

.dark .card{
background:#3b2430;
color:white;
}

.dark .newsletter{
background:#4b2132;
}

.dark footer{
background:#1d1016;
}const botao = document.getElementById("tema");

botao.onclick = () => {
    document.body.classList.toggle("dark");

    if(document.body.classList.contains("dark")){
        botao.textContent = "☀️";
    }else{
        botao.textContent = "🌙";
    }
}
