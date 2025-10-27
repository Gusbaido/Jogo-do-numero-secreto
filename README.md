# 🎯 Jogo do Número Secreto

Um projeto simples e divertido desenvolvido em **JavaScript**, **HTML** e **CSS**, onde o jogador tenta adivinhar o número secreto gerado aleatoriamente pelo sistema.  
Ideal para praticar **lógica de programação**, **funções**, **condições** e **interação com o DOM**.

---

## 🧠 Objetivo do Jogo

Descobrir o número secreto entre **1 e 10** (ou outro limite definido).  
A cada tentativa, o jogo informa se o número secreto é **maior ou menor** do que o chute.  
Quando o jogador acerta, o jogo exibe o número de tentativas e permite **reiniciar a partida**.

---

## 🧩 Tecnologias Utilizadas

- **HTML5** → estrutura da página  
- **CSS3** → estilização visual (não exibido aqui, mas pode ser adicionado)  
- **JavaScript (ES6+)** → lógica do jogo e manipulação do DOM  
- **[ResponsiveVoice.js](https://responsivevoice.org/)** → biblioteca de leitura de texto em voz (fala o que aparece na tela)

---

## ⚙️ Funcionalidades Principais

### 🔹 `exibirTextoNaTela(tag, texto)`
Exibe o texto dinamicamente na tela, dentro da tag indicada (`h1`, `p`, etc.), e lê a mensagem com voz.

### 🔹 `exibirMensagemInicial()`
Mostra a mensagem padrão de início do jogo:
Jogo do número secreto
Escolha um número entre 1 e 10

markdown
Copiar código

### 🔹 `verificarChute()`
Compara o número digitado com o número secreto:
- Se acertar → exibe mensagem de sucesso e número de tentativas.  
- Se errar → informa se o número secreto é **maior** ou **menor**.

Também habilita o botão de **reiniciar** após a vitória.

### 🔹 `gerarNumeroAleatorio()`
Gera um número aleatório entre 1 e o limite (`numeroLimite`), sem repetir números até todos terem sido sorteados.  
Usa uma lista (`listaDeNumerosSorteados`) para garantir que cada número só aparece uma vez por ciclo.

### 🔹 `limparCampo()`
Limpa o campo de entrada de texto após cada tentativa.

### 🔹 `reiniciarJogo()`
Reinicia o jogo:
- Gera novo número secreto  
- Reseta o contador de tentativas  
- Exibe novamente a mensagem inicial  
- Desativa o botão de “Reiniciar” até o próximo acerto

---

## 🧮 Lógica de Geração do Número Secreto

```javascript
let numeroEscolhido = parseInt(Math.random() * numeroLimite + 1);
Math.random() → gera número aleatório entre 0 e 1.

Multiplicado por numeroLimite e somado com 1 → garante que o número esteja entre 1 e o limite (inclusive).

parseInt() → converte o resultado para número inteiro.

🚀 Como Executar
Crie um arquivo index.html com o layout do jogo (input, botão de chute e botão de reiniciar).

Inclua este script JavaScript no final do <body>.

Adicione o link da biblioteca ResponsiveVoice no HTML:

html
Copiar código
<script src="https://code.responsivevoice.org/responsivevoice.js?key=YOUR_KEY"></script>
Abra o arquivo index.html no navegador.

Digite um número e tente adivinhar o número secreto!

🗂️ Estrutura Sugerida de Pastas
pgsql
Copiar código
📁 jogo-numero-secreto
├── index.html
├── script.js
└── style.css
💬 Exemplo de Mensagens na Tela
Situação	Mensagem exibida
Início do jogo	“Escolha um número entre 1 e 10”
Acertou	“Acertou! Você descobriu o número secreto com X tentativas!”
Errou (maior)	“O número secreto é menor”
Errou (menor)	“O número secreto é maior”

🧑‍💻 Autor
Desenvolvido por Gustavo Baido — estudante de Engenharia da Computação e analista de dados, explorando o mundo da programação com projetos práticos e divertidos.
