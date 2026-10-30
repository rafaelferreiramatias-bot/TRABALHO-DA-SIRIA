<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Exemplo HTML, CSS e DOM</title>

    <style>
        body {
            margin: 0;
            font-family: Arial, sans-serif;
        }

        header {
            background-color: lightblue;
            padding: 20px;
        }

        nav {
            background-color: lightgray;
            padding: 15px;
        }

        main {
            background-color: white;
            padding: 20px;
            min-height: 200px;
        }

        footer {
            background-color: gray;
            padding: 20px;
        }

        .bloco-footer {
            padding: 15px;
            margin: 10px;
        }

        #bloco1 {
            background-color: lightcoral;
        }

        #bloco2 {
            background-color: lightgreen;
        }

        #bloco3 {
            background-color: lightyellow;
        }
    </style>
</head>

<body>

    <header>
        <h1>Meu Site</h1>
    </header>

    <nav>
        <a href="#">Início</a>
        <a href="#">Sobre</a>
        <a href="#">Contato</a>
    </nav>

    <main id="conteudo">
        <!-- O JavaScript criará os elementos aqui -->
    </main>


    <script>
        const main = document.getElementById("conteudo");

        main.style.textAlign = "center";

        const titulo = document.createElement("h2");
        titulo.textContent = "Feira das Nações: Portugal";
        main.appendChild(titulo);

        const imagem = document.createElement("img");
        imagem.src = "https://thumb.wikimedia.org/wikipedia/commons/thumb/a/a8/Flag_of_Portugal_%28official%29.svg/330px-Flag_of_Portugal_%28official%29.svg.png?utm_source=pt.wikipedia.org&utm_campaign=parser&utm_content=thumbnail";
        imagem.alt = "Bandeira de Portugal";
        imagem.style.width = "150px";
        imagem.style.display = "block";
        imagem.style.margin = "15px auto";
        imagem.style.borderRadius = "4px";
        imagem.style.boxShadow = "0px 2px 5px rgba(0,0,0,0.2)";
        main.appendChild(imagem);

        const tituloCultura = document.createElement("h3");
        tituloCultura.textContent = "A Rica Cultura Portuguesa";
        tituloCultura.style.marginTop = "25px";
        main.appendChild(tituloCultura);

        const textoCultura = document.createElement("p");
        textoCultura.textContent = "A cultura de Portugal é profundamente ligada à sua história marítima. É famosa mundialmente pelo Fado, um estilo musical melancólico e emocionante que expressa a 'saudade'. O país também se destaca pela arte dos azulejos pintados à mão que decoram ruas e igrejas, além de uma rica literatura e uma forte tradição de hospitalidade familiar.";
        textoCultura.style.maxWidth = "600px";
        textoCultura.style.margin = "10px auto 25px auto";
        textoCultura.style.lineHeight = "1.6";
        main.appendChild(textoCultura);

        const subheader = document.createElement("h3");
        subheader.textContent = "Curiosidades sobre o País:";
        main.appendChild(subheader);

        const listaOrdenada = document.createElement("ol");
        listaOrdenada.style.display = "inline-block";
        listaOrdenada.style.textAlign = "left";
        listaOrdenada.style.margin = "0 auto";

        const item1 = document.createElement("li");
        item1.textContent = "Paixão pelo Futebol: Portugal é a terra de grandes craques mundiais, como Cristiano Ronaldo e Eusébio.";
        listaOrdenada.appendChild(item1);

        const item2 = document.createElement("li");
        item2.textContent = "Gastronomia Famosa: O país é conhecido internacionalmente pelos deliciosos Pastéis de Nata e pratos com Bacalhau.";
        listaOrdenada.appendChild(item2);

        const item3 = document.createElement("li");
        item3.textContent = "História dos Navegadores: Foi um dos pioneiros na Era dos Descobrimentos, explorando rotas marítimas pelo mundo inteiro.";
        listaOrdenada.appendChild(item3);

        main.appendChild(listaOrdenada);

        const topoSite = document.querySelector("header");
        const menuNavegacao = document.querySelector("nav");

        if (topoSite) {
            topoSite.style.textAlign = "center";
        }
        if (menuNavegacao) {
            menuNavegacao.style.textAlign = "center";
        }

        if (topoSite) {
            topoSite.style.backgroundColor = "#00662F"; 
            topoSite.style.color = "#FFFFFF";
        }
        if (menuNavegacao) {
            menuNavegacao.style.backgroundColor = "#1D8443";
            const links = menuNavegacao.querySelectorAll("a");
            links.forEach(link => {
                link.style.color = "#FFFFFF";
                link.style.margin = "0 10px";
                link.style.textDecoration = "none";
                link.style.fontWeight = "bold";
            });
        }

        main.style.backgroundColor = "#FDFBF7";
        main.style.color = "#333333";

        const rodape = document.querySelector("footer");
        if (rodape) {
            rodape.style.backgroundColor = "#D2151E";
            rodape.style.display = "flex";
            rodape.style.justifyContent = "center";
        }

        const b1 = document.getElementById("bloco1");
        const b2 = document.getElementById("bloco2");
        const b3 = document.getElementById("bloco3");

        if (b1) {
            b1.style.backgroundColor = "#FFD700";
            b1.style.color = "#000000";
        }
        if (b2) {
            b2.style.backgroundColor = "#FFFFFF";
            b2.style.color = "#000000";
        }
        if (b3) {
            b3.style.backgroundColor = "#FFD700";
            b3.style.color = "#000000";
        }
    </script>

</body>
</html>
