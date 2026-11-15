# 💼 Portfólio Profissional – Alendre Luciano Silveira

Site de portfólio pessoal feito com **HTML5, CSS3, Bootstrap e JavaScript** para apresentar o meu perfil, a minha trajetória, os meus projetos e as formas de contato, unindo mais de 20 anos de experiência industrial ao Desenvolvimento de Sistemas.

## 👤 Autor

| | |
|---|---|
| **Nome** | Alendre Luciano Silveira |
| **RM** | SP26AO0263317 |
| **Turma** | FML – 1º DS |
| **Curso** | Técnico em Desenvolvimento de Sistemas – ETEC |
| **Atividade** | Agenda 15 – Portfólio: um projeto do início ao fim |

## 🎯 Objetivo da atividade

Desenvolver ou atualizar o portfólio pessoal, usando como base o projeto construído em aula, deixando o site mais completo, personalizado e com novos recursos, contendo:

- **Seção de Perfil**;
- **Seção de Projetos**;
- **Seção de Contato**;
- **Menu de navegação** funcional;
- uso do **Bootstrap**;
- publicação no **GitHub Pages**;
- pelo menos **um recurso novo**, além do que foi feito em aula.

## 📝 Descrição do portfólio

O portfólio é um site de uma página só. Ele mostra a minha transição de carreira: sou Técnico em Processos, com mais de 20 anos nas indústrias aeronáutica e industrial, sendo quase 18 anos na Embraer, onde passei pela produção, Métodos e Processos, Tempos e Métodos, PCP e implantação do SAP. Hoje estudo Desenvolvimento de Sistemas.

O site começou com o modelo construído em aula e foi evoluído com informações reais sobre a minha carreira, os meus projetos do GitHub, as cores do meu infocurrículo e cinco recursos novos.

## 🔗 Link do site publicado

| | |
|---|---|
| **Site (GitHub Pages)** | https://alendre-sjc.github.io/portfolio/ |
| **Repositório** | https://github.com/alendre-sjc/portfolio |

## 📁 Estrutura do projeto

```
portfolio/
 |-- index.html        => página principal (código comentado Ato por Ato)
 |-- README.md         => este arquivo de descrição
 |-- arquivos/         => arquivos para download
 |    '-- curriculo-alendre-silveira.pdf
 '-- imagens/          => imagens usadas na página
      |-- perfil.png
      |-- slide1.png, slide2.png, slide3.png
      |-- p1.png, p2.png, p3.png
      '-- compartilhar.png
```

## ⚙️ Como o projeto funciona

O código do `index.html` está todo comentado **Ato por Ato** (do Ato 0 ao Ato 14), na ordem em que o navegador lê a página. A página é dividida em partes:

| Parte | O que mostra |
|---|---|
| **Menu (navbar)** | Fixo no topo. Leva para cada seção e vira um botão no celular |
| **Carousel** | 3 slides com título, texto e botões, incluindo "Baixar currículo" |
| **Perfil** | Foto, apresentação, as duas frentes da carreira, informações, tecnologias e ferramentas |
| **Trajetória** | Linha do tempo da experiência profissional e da formação |
| **Projetos** | 3 projetos reais do meu GitHub, com botão para o repositório |
| **Contato** | Áreas de interesse e botões de currículo, e-mail, GitHub, LinkedIn e WhatsApp |
| **Rodapé** | Direitos autorais e tecnologias usadas |

Os links do menu usam `href="#nome-da-secao"`, que leva até a seção que tem o `id` com o mesmo nome. Os botões de currículo usam o atributo `download`, que faz o navegador baixar o PDF.

## 🛠️ Tecnologias utilizadas

| Tecnologia | Para que foi usada |
|---|---|
| **HTML5** | Estrutura da página |
| **CSS3** | Cores, animações e estilos personalizados |
| **Bootstrap 5.3** | Layout responsivo, menu, carousel, cards e botões |
| **JavaScript** | Botão "voltar ao topo" |
| **Devicon** | Ícones das tecnologias |
| **Bootstrap Icons** | Ícones das ferramentas da carreira industrial |
| **Git e GitHub** | Versionamento do código |
| **GitHub Pages** | Publicação do site |

## 🏷️ Tags, classes e atributos principais

| Tag / Classe | Para que serve | Atributos usados |
|---|---|---|
| `<nav class="navbar">` | Menu de navegação | `navbar-expand-lg`, `sticky-top` |
| `<div class="carousel">` | Slides de destaque | `data-bs-ride`, `data-bs-target` |
| `<section>` | Cada seção da página | `id="perfil"`, `id="contato"`... |
| `row` / `col-*` | Grid do Bootstrap (linhas e colunas) | `col-lg-4`, `col-md-6`... |
| `card` | Blocos com borda e sombra | `card-body`, `shadow-sm` |
| `badge` | Etiquetas coloridas | `bg-primary`, `bg-dark` |
| `<img>` | Mostra as imagens | `src`, `alt` |
| `<i>` | Ícones (Devicon e Bootstrap Icons) | `class="devicon-..."`, `class="bi bi-..."` |
| `<a>` | Links e botões | `href`, `target="_blank"`, `download` |
| `<style>` | CSS interno com as cores e os recursos novos | — |
| `<script>` | JavaScript do Bootstrap e do botão "voltar ao topo" | `src` |
| `<!-- -->` | Comentário (não aparece na página) | — |

## ✨ Recursos novos adicionados

| Nº | Recurso | O que faz |
|---|---|---|
| 1 | **Legenda animada no carousel** | O título, o texto e os botões de cada slide sobem e aparecem suavemente |
| 2 | **Animação nos cards de projetos** | Ao passar o mouse, o card sobe e ganha uma sombra maior |
| 3 | **Seção Trajetória** | Linha do tempo com a minha experiência profissional e a minha formação |
| 4 | **Botão "voltar ao topo"** | Aparece ao rolar a página e leva de volta ao início |
| 5 | **Cores do meu infocurrículo** | Azul-marinho e verde-azulado no lugar das cores padrão do Bootstrap |

## 🔧 Como os recursos foram implementados

### 1. Legenda animada no carousel

No CSS, criei uma animação chamada `surgir` com `@keyframes`. Ela começa invisível (`opacity: 0`) e 40px abaixo, e termina visível na posição normal. A animação só roda no slide ativo:

```css
.carousel-item.active .carousel-caption {
    animation: surgir 1s ease;
}

@keyframes surgir {
    from { opacity: 0; transform: translateY(40px); }
    to   { opacity: 1; transform: translateY(0); }
}
```

### 2. Animação nos cards (hover)

Criei a classe `card-animado` e coloquei nos três cards de projetos. O `transition` faz a mudança acontecer devagar e o `:hover` diz o que muda quando o mouse está em cima:

```css
.card-animado {
    transition: transform 0.3s, box-shadow 0.3s;
}

.card-animado:hover {
    transform: translateY(-10px);
    box-shadow: 0 1rem 2rem rgba(0, 0, 0, 0.2) !important;
}
```

### 3. Seção Trajetória

Criei uma nova `section` com `id="trajetoria"` e um link no menu. Uma `row` do Bootstrap divide o espaço em duas colunas (`col-lg-7` para a experiência e `col-lg-5` para a formação). A linha do tempo foi feita só com CSS: a borda da esquerda vira a linha vertical e o `::before` desenha uma bolinha em cada item:

```css
.linha-tempo {
    border-left: 4px solid #087E86;
    padding-left: 30px;
}

.item-tempo::before {
    content: "";
    position: absolute;
    left: -42px;
    width: 20px;
    height: 20px;
    background-color: #087E86;
    border-radius: 50%;
}
```

### 4. Botão voltar ao topo

No HTML, um link com `id="btnTopo"` e `href="#"`. No CSS, ele fica fixo no canto (`position: fixed`) e começa escondido (`display: none`). O JavaScript mostra o botão quando a página desce mais de 300 pixels:

```javascript
let botao = document.getElementById("btnTopo");

window.onscroll = function () {
    if (window.scrollY > 300) {
        botao.style.display = "block";
    } else {
        botao.style.display = "none";
    }
};
```

### 5. Cores do meu infocurrículo

Reescrevi algumas classes do Bootstrap com as minhas cores, usando `!important` para que elas tenham prioridade:

```css
.bg-dark {
    background-color: #102B46 !important;   /* azul-marinho */
}

.text-primary {
    color: #087E86 !important;              /* verde-azulado */
}
```

O mesmo foi feito em `.bg-light`, `.bg-primary`, `.btn-primary`, `.btn-dark` e `.btn-outline-primary`. Também criei a classe `.titulo-secao`, que deixa os títulos em maiúsculas com um tracinho embaixo.

## ▶️ Como executar

1. Baixe ou clone este repositório.
2. Abra a pasta do projeto.
3. Dê dois cliques no arquivo `index.html` e a página abrirá no navegador.

Pelo terminal do VS Code, dentro da pasta do projeto:

```
start index.html
```

Ou acesse direto o site publicado: https://alendre-sjc.github.io/portfolio/

## 📌 Fonte das imagens

Foto de perfil e currículo de autoria própria. Imagens do carousel e dos projetos criadas para o portfólio. Ícones das bibliotecas Devicon e Bootstrap Icons, usados apenas para fins de estudo.

## 🧰 Ferramentas utilizadas

- **HTML5, CSS3 e JavaScript**
- **Bootstrap 5.3**
- **Visual Studio Code**
- **Google Chrome**
- **Git e GitHub**
