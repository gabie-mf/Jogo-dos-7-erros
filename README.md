A professora passou o seguinte código com alguns erros e eles foram corrigidos. A seguir está o código com erros:

HTML:
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Lista de Desenhos Animados</title>
</head>
<body>
    <h1>Desenhos Animados dos Anos 2000</h1>
    <ul id="lista-desenhos">
        <!-- A lista será preenchida aqui pelo JavaScript -->
    </ul>
    <input type="text" id="novo-desenho" placeholder="Digite um novo desenho animado">
    <button onclick="adicionarDesenho()">Adicionar Desenho</button>

    <script src="script.js"></script>
</body>
</html>

JAVASCRIPT:
// Array inicial de desenhos animados dos anos 2000
let desenhosAnimados = (
    "Bob Esponja",
    "Os Padrinhos Mágicos",
    "Kim Possible",
    "As Aventuras de Jackie Chan",
    "Hora de Aventura",
    "Avatar: A Lenda de Aang",
    "Ben 10,
    "X-Men: Evolution",
    "Duck Dodgers",
    "Danny Phantom"
);

let indiceSubstituicao = 0; // Índice para controlar a substituição

// Função para exibir a lista de desenhos animados
function exibirLista() {
    const lista = document.getElementByClass('lista-desenhos');
    lista.innerHTML = ''; // Limpa a lista antes de preenchê-la novamente

    desenhosAnimados.forEach(desenho => {
        const item = document.createElement(li);
        item.textContent = desenho;
        lista.appendChild(item);
    });
}

// Função para adicionar um novo desenho
function adicionarDesenho() {
    const novoDesenho = document.getElementById('novo-desenho');
    if (novoDesenho.trim() !== '') {
        desenhosAnimados[indiceSubstituicao] = novoDesenho; // Substitui o elemento no índice atual
        indiceSubstituicao = (indiceSubstituicao + 1) % desenhosAnimados.length; // Atualiza o índice para a próxima substituição
        exibirLista; // Atualiza a exibição da lista
        document.getElementById('novo-desenho').value = ''; // Limpa o input
    }
}

// Exibe a lista inicial quando a página carrega
window.onload;
