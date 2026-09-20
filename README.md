# <!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Porcel Shop</title>

<style>
*{
    margin:0;
    padding:0;
    box-sizing:border-box;
    font-family:Arial,Helvetica,sans-serif;
}

body{
    background:#080b12;
    color:#fff;
    min-height:100vh;
}

header{
    position:sticky;
    top:0;
    z-index:1000;
    background:#0e1420;
    border-bottom:1px solid #263148;
    padding:15px;
}

.topo{
    max-width:1100px;
    margin:auto;
    display:flex;
    justify-content:space-between;
    align-items:center;
    gap:15px;
}

.logo{
    font-size:24px;
    font-weight:900;
    color:#2da8ff;
}

.logo span{
    color:#fff;
}

nav{
    display:flex;
    gap:6px;
}

nav button{
    border:0;
    background:transparent;
    color:#aaa;
    padding:9px;
    cursor:pointer;
}

nav button:hover{
    color:#2da8ff;
}

.container{
    width:92%;
    max-width:1100px;
    margin:auto;
}

.pagina{
    min-height:80vh;
}

.hero{
    text-align:center;
    padding:55px 0 35px;
}

.hero h1{
    font-size:42px;
    margin-bottom:12px;
}

.hero h1 span{
    color:#2da8ff;
}

.hero p{
    color:#8f9aae;
    margin-bottom:25px;
}

.busca{
    width:100%;
    max-width:650px;
    padding:16px;
    border-radius:13px;
    border:1px solid #2a354b;
    background:#111827;
    color:#fff;
    font-size:16px;
    outline:none;
}

.secao{
    padding:25px 0 60px;
}

.titulo{
    display:flex;
    justify-content:space-between;
    align-items:center;
    margin-bottom:20px;
}

.titulo h2{
    font-size:27px;
}

.produtos{
    display:grid;
    grid-template-columns:repeat(auto-fill,minmax(230px,1fr));
    gap:20px;
}

.card{
    background:#111722;
    border:1px solid #222e43;
    border-radius:17px;
    overflow:hidden;
    transition:.2s;
}

.card:hover{
    transform:translateY(-4px);
    border-color:#2da8ff;
}

.card-imagem{
    width:100%;
    height:220px;
    object-fit:cover;
    display:block;
    background:#080b12;
}

.sem-imagem{
    height:220px;
    display:flex;
    justify-content:center;
    align-items:center;
    color:#667188;
    font-size:40px;
}

.card-conteudo{
    padding:17px;
}

.card h3{
    margin-bottom:8px;
}

.descricao{
    color:#929caf;
    font-size:14px;
    line-height:1.4;
    min-height:40px;
    margin-bottom:13px;
}

.preco{
    color:#2da8ff;
    font-size:23px;
    font-weight:bold;
    margin-bottom:15px;
}

.btn{
    border:0;
    border-radius:10px;
    padding:12px 16px;
    font-weight:bold;
    cursor:pointer;
}

.btn:hover{
    opacity:.88;
}

.btn-principal{
    background:#2da8ff;
    color:#03111c;
}

.btn-whatsapp{
    background:#20c967;
    color:white;
    width:100%;
}

.btn-editar{
    background:#f59e0b;
    color:white;
}

.btn-excluir{
    background:#ef4444;
    color:white;
}

.btn-voltar{
    background:#202b3f;
    color:white;
}

.painel{
    display:none;
}

.caixa{
    background:#111722;
    border:1px solid #222e43;
    border-radius:17px;
    padding:22px;
    margin:30px 0;
}

.caixa h2{
    margin-bottom:20px;
}

label{
    display:block;
    color:#adb7c8;
    font-size:14px;
    margin-bottom:7px;
}

input,
textarea{
    width:100%;
    padding:14px;
    margin-bottom:17px;
    border-radius:10px;
    border:1px solid #29364d;
    background:#080d16;
    color:#fff;
    outline:none;
    font-size:15px;
}

textarea{
    min-height:100px;
    resize:vertical;
}

#campoImagem{
    display:none;
}

.botao-galeria{
    display:flex;
    align-items:center;
    justify-content:center;
    width:100%;
    min-height:55px;
    background:#202b3f;
    border:1px dashed #4b5c78;
    border-radius:12px;
    color:white;
    cursor:pointer;
    margin-bottom:15px;
}

.botao-galeria:hover{
    background:#29364b;
}

.preview{
    width:200px;
    height:200px;
    object-fit:cover;
    border-radius:14px;
    display:none;
    margin:0 auto 18px;
}

.mensagem{
    margin-top:12px;
    color:#2da8ff;
}

.lista-admin{
    margin-top:20px;
}

.admin-item{
    display:flex;
    align-items:center;
    gap:12px;
    background:#0c121d;
    border-radius:12px;
    padding:12px;
    margin-bottom:10px;
}

.admin-item img{
    width:70px;
    height:70px;
    object-fit:cover;
    border-radius:9px;
}

.admin-info{
    flex:1;
}

.admin-info strong{
    display:block;
    margin-bottom:6px;
}

.admin-info span{
    color:#2da8ff;
}

.acoes{
    display:flex;
    gap:7px;
}

.vazio{
    text-align:center;
    color:#788398;
    padding:45px 10px;
    grid-column:1/-1;
}

footer{
    border-top:1px solid #202a3d;
    padding:30px 15px;
    text-align:center;
    color:#687387;
}

.escondido{
    display:none !important;
}

@media(max-width:650px){

    .topo{
        flex-direction:column;
    }

    nav{
        width:100%;
        justify-content:center;
    }

    .hero h1{
        font-size:32px;
    }

    .produtos{
        grid-template-columns:1fr 1fr;
        gap:12px;
    }

    .card-imagem,
    .sem-imagem{
        height:170px;
    }

    .card-conteudo{
        padding:12px;
    }

    .card h3{
        font-size:16px;
    }

    .preco{
        font-size:19px;
    }

    .admin-item{
        flex-wrap:wrap;
    }

    .acoes{
        width:100%;
    }

    .acoes button{
        flex:1;
    }
}

@media(max-width:420px){

    .produtos{
        grid-template-columns:1fr;
    }

    .card-imagem,
    .sem-imagem{
        height:220px;
    }
}
</style>
</head>

<body>

<header>

<div class="topo">

<div class="logo">
PORCEL <span>SHOP</span>
</div>

<nav>
<button onclick="mostrarInicio()">Início</button>
<button onclick="mostrarProdutos()">Produtos</button>
<button onclick="abrirPainel()">➕ Adicionar</button>
</nav>

</div>

</header>


<!-- ==============================
     INÍCIO
================================ -->

<main id="inicio" class="pagina">

<div class="container">

<section class="hero">

<h1>
Bem-vindo ao <span>Porcel Shop</span>
</h1>

<p>
Encontre produtos e fale diretamente com o vendedor.
</p>

<input
id="buscaInicio"
class="busca"
type="search"
placeholder="🔎 Pesquisar produto..."
oninput="pesquisar()"
>

</section>

<section class="secao">

<div class="titulo">
<h2>Produtos</h2>
</div>

<div id="produtosInicio" class="produtos"></div>

</section>

</div>

</main>


<!-- ==============================
     PRODUTOS
================================ -->

<main id="paginaProdutos" class="pagina escondido">

<div class="container">

<section class="secao">

<div class="titulo">
<h2>Todos os produtos</h2>

<button
class="btn btn-voltar"
onclick="mostrarInicio()"
>
Voltar
</button>

</div>

<input
id="buscaProdutos"
class="busca"
type="search"
placeholder="🔎 Pesquisar produto..."
oninput="pesquisar()"
>

<br><br>

<div id="todosProdutos" class="produtos"></div>

</section>

</div>

</main>


<!-- ==============================
     PAINEL
================================ -->

<main id="paginaPainel" class="painel">

<div class="container">

<section class="secao">

<div class="caixa">

<div class="titulo">

<h2>➕ Adicionar produto</h2>

<button
class="btn btn-voltar"
onclick="mostrarInicio()"
>
Voltar
</button>

</div>


<!--
     ESTE BOTÃO ABRE DIRETAMENTE
     A GALERIA DO CELULAR
-->

<label
for="campoImagem"
class="botao-galeria"
>
📸 Escolher imagem da galeria
</label>

<input
id="campoImagem"
type="file"
accept="image/*"
onchange="escolherImagem(event)"
>


<img
id="preview"
class="preview"
>


<label>Nome do produto</label>

<input
id="nome"
type="text"
placeholder="Ex: Armário de cozinha"
>


<label>Preço</label>

<input
id="preco"
type="number"
step="0.01"
placeholder="Ex: 599.90"
>


<label>Descrição</label>

<textarea
id="descricao"
placeholder="Digite as informações do produto..."
></textarea>


<label>WhatsApp</label>

<input
id="whatsapp"
type="tel"
placeholder="Ex: 5516999999999"
>


<button
class="btn btn-principal"
onclick="adicionarProduto()"
>
✅ Adicionar produto
</button>

<p id="mensagem" class="mensagem"></p>

</div>


<div class="caixa">

<h2>📦 Produtos cadastrados</h2>

<div id="listaAdmin" class="lista-admin"></div>

</div>

</section>

</div>

</main>


<footer>

Porcel Shop © 2026

</footer>


<script>

/* =====================================
   PRODUTOS
===================================== */

let produtos =
JSON.parse(
    localStorage.getItem("porcelShopProdutos")
) || [];

let imagemAtual = "";


/* =====================================
   SALVAR
===================================== */

function salvar(){

    localStorage.setItem(
        "porcelShopProdutos",
        JSON.stringify(produtos)
    );

}


/* =====================================
   ESCOLHER IMAGEM
===================================== */

function escolherImagem(event){

    const arquivo =
        event.target.files[0];

    if(!arquivo){
        return;
    }

    if(!arquivo.type.startsWith("image/")){

        alert("Escolha uma imagem.");

        event.target.value = "";

        return;
    }


    const leitor =
        new FileReader();


    leitor.onload = function(e){

        imagemAtual =
            e.target.result;


        const preview =
            document.getElementById("preview");


        preview.src =
            imagemAtual;


        preview.style.display =
            "block";

    };


    leitor.readAsDataURL(arquivo);

}


/* =====================================
   ADICIONAR
===================================== */

function adicionarProduto(){

    const nome =
        document.getElementById("nome")
        .value
        .trim();

    const preco =
        document.getElementById("preco")
        .value;

    const descricao =
        document.getElementById("descricao")
        .value
        .trim();

    const whatsapp =
        document.getElementById("whatsapp")
        .value
        .trim();


    if(!imagemAtual){

        alert(
            "Primeiro escolha uma imagem da galeria."
        );

        return;
    }


    if(!nome){

        alert(
            "Digite o nome do produto."
        );

        return;
    }


    if(!preco){

        alert(
            "Digite o preço."
        );

        return;
    }


    if(!whatsapp){

        alert(
            "Digite o WhatsApp."
        );

        return;
    }


    const produto = {

        id:Date.now(),

        imagem:imagemAtual,

        nome:nome,

        preco:Number(preco),

        descricao:descricao,

        whatsapp:whatsapp

    };


    produtos.unshift(produto);

    salvar();

    limparFormulario();

    atualizarTudo();


    document.getElementById("mensagem")
        .textContent =
        "✅ Produto adicionado!";


    setTimeout(function(){

        document.getElementById("mensagem")
            .textContent = "";

    },3000);

}


/* =====================================
   LIMPAR
===================================== */

function limparFormulario(){

    document.getElementById("campoImagem")
        .value = "";

    document.getElementById("nome")
        .value = "";

    document.getElementById("preco")
        .value = "";

    document.getElementById("descricao")
        .value = "";

    document.getElementById("whatsapp")
        .value = "";

    document.getElementById("preview")
        .style.display = "none";

    imagemAtual = "";

}


/* =====================================
   CARD
===================================== */

function criarCard(produto){

    const preco =
        Number(produto.preco)
        .toLocaleString(
            "pt-BR",
            {
                style:"currency",
                currency:"BRL"
            }
        );


    return `

    <article class="card">

        ${
            produto.imagem

            ?

            `
            <img
                class="card-imagem"
                src="${produto.imagem}"
                alt="${produto.nome}"
            >
            `

            :

            `
            <div class="sem-imagem">
                📦
            </div>
            `
        }


        <div class="card-conteudo">

            <h3>
                ${produto.nome}
            </h3>

            <p class="descricao">
                ${produto.descricao || "Sem descrição."}
            </p>

            <div class="preco">
                ${preco}
            </div>

            <button
                class="btn btn-whatsapp"
                onclick="abrirWhatsApp(${produto.id})"
            >
                💬 Tenho interesse
            </button>

        </div>

    </article>

    `;

}


/* =====================================
   WHATSAPP
===================================== */

function abrirWhatsApp(id){

    const produto =
        produtos.find(
            item => item.id === id
        );


    if(!produto){
        return;
    }


    const numero =
        produto.whatsapp
        .replace(/\D/g,"");


    const texto =
        `Olá! Tenho interesse no produto "${produto.nome}" do Porcel Shop.`;


    const link =
        "https://wa.me/" +
        numero +
        "?text=" +
        encodeURIComponent(texto);


    window.open(
        link,
        "_blank"
    );

}


/* =====================================
   MOSTRAR PRODUTOS
===================================== */

function atualizarProdutos(){

    const areaInicio =
        document.getElementById(
            "produtosInicio"
        );

    const areaTodos =
        document.getElementById(
            "todosProdutos"
        );


    if(produtos.length === 0){

        const mensagem = `
            <div class="vazio">
                📦<br><br>
                Ainda não existem produtos.
            </div>
        `;

        areaInicio.innerHTML =
            mensagem;

        areaTodos.innerHTML =
            mensagem;

        return;
    }


    areaInicio.innerHTML =
        produtos
        .slice(0,8)
        .map(criarCard)
        .join("");


    areaTodos.innerHTML =
        produtos
        .map(criarCard)
        .join("");

}


/* =====================================
   PAINEL ADMIN
===================================== */

function atualizarPainel(){

    const area =
        document.getElementById(
            "listaAdmin"
        );


    if(produtos.length === 0){

        area.innerHTML = `
            <div class="vazio">
                Nenhum produto cadastrado.
            </div>
        `;

        return;
    }


    area.innerHTML =
        produtos.map(produto => `

        <div class="admin-item">

            <img
                src="${produto.imagem}"
                alt="${produto.nome}"
            >

            <div class="admin-info">

                <strong>
                    ${produto.nome}
                </strong>

                <span>
                    ${Number(produto.preco)
                    .toLocaleString(
                        "pt-BR",
                        {
                            style:"currency",
                            currency:"BRL"
                        }
                    )}
                </span>

            </div>


            <div class="acoes">

                <button
                    class="btn btn-editar"
                    onclick="editarProduto(${produto.id})"
                >
                    ✏️
                </button>

                <button
                    class="btn btn-excluir"
                    onclick="excluirProduto(${produto.id})"
                >
                    🗑️
                </button>

            </div>

        </div>

    `).join("");

}


/* =====================================
   EDITAR
===================================== */

function editarProduto(id){

    const produto =
        produtos.find(
            item => item.id === id
        );


    if(!produto){
        return;
    }


    const novoNome =
        prompt(
            "Nome do produto:",
            produto.nome
        );


    if(novoNome === null){
        return;
    }


    const novoPreco =
        prompt(
            "Preço:",
            produto.preco
        );


    if(novoPreco === null){
        return;
    }


    const novaDescricao =
        prompt(
            "Descrição:",
            produto.descricao
        );


    if(novaDescricao === null){
        return;
    }


    const novoWhatsApp =
        prompt(
            "WhatsApp:",
            produto.whatsapp
        );


    if(novoWhatsApp === null){
        return;
    }


    produto.nome =
        novoNome;

    produto.preco =
        Number(novoPreco);

    produto.descricao =
        novaDescricao;

    produto.whatsapp =
        novoWhatsApp;


    salvar();

    atualizarTudo();


    alert(
        "Produto atualizado!"
    );

}


/* =====================================
   EXCLUIR
===================================== */

function excluirProduto(id){

    const confirmar =
        confirm(
            "Tem certeza que deseja excluir este produto?"
        );


    if(!confirmar){
        return;
    }


    produtos =
        produtos.filter(
            item => item.id !== id
        );


    salvar();

    atualizarTudo();

}


/* =====================================
   PESQUISA
===================================== */

function pesquisar(){

    const campoInicio =
        document.getElementById(
            "buscaInicio"
        );

    const campoProdutos =
        document.getElementById(
            "buscaProdutos"
        );


    let termo = "";


    if(
        !document
        .getElementById("inicio")
        .classList
        .contains("escondido")
    ){

        termo =
            campoInicio.value
            .toLowerCase()
            .trim();

    }else{

        termo =
            campoProdutos.value
            .toLowerCase()
            .trim();

    }


    const encontrados =
        produtos.filter(produto => {

            const nome =
                produto.nome
                .toLowerCase();

            const descricao =
                produto.descricao
                .toLowerCase();


            return (
                nome.includes(termo) ||
                descricao.includes(termo)
            );

        });


    document.getElementById(
        "produtosInicio"
    ).innerHTML =

        encontrados
        .slice(0,8)
        .map(criarCard)
        .join("");


    document.getElementById(
        "todosProdutos"
    ).innerHTML =

        encontrados
        .map(criarCard)
        .join("");

}


/* =====================================
   NAVEGAÇÃO
===================================== */

function esconderPaginas(){

    document
        .getElementById("inicio")
        .classList
        .add("escondido");


    document
        .getElementById("paginaProdutos")
        .classList
        .add("escondido");


    document
        .getElementById("paginaPainel")
        .style
        .display = "none";

}


function mostrarInicio(){

    esconderPaginas();

    document
        .getElementById("inicio")
        .classList
        .remove("escondido");

}


function mostrarProdutos(){

    esconderPaginas();

    document
        .getElementById("paginaProdutos")
        .classList
        .remove("escondido");

}


function abrirPainel(){

    esconderPaginas();

    document
        .getElementById("paginaPainel")
        .style
        .display = "block";

    atualizarPainel();

}


/* =====================================
   ATUALIZAR TUDO
===================================== */

function atualizarTudo(){

    atualizarProdutos();

    atualizarPainel();

}


/* =====================================
   INICIAR
===================================== */

atualizarTudo();

</script>

</body>
</html>-
