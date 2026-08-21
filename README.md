# XBRGAMES

> Plataforma web para apresentação e distribuição de projetos de jogos desenvolvidos para navegador.

![XBRGAMES](assets/00000002.svg)

## Sobre o projeto

**XBRGAMES** é uma plataforma criada para centralizar, apresentar e disponibilizar projetos de jogos desenvolvidos para a web.

O projeto funciona como uma espécie de **hub de jogos**, combinando uma landing page moderna com animações, apresentação visual dos projetos, introdução em vídeo e acesso direto às demos.

A proposta é proporcionar uma experiência semelhante à de uma pequena plataforma independente de jogos, onde cada projeto pode ser apresentado individualmente e executado diretamente pelo navegador.

## Projetos

Atualmente, a plataforma apresenta os seguintes projetos:

### Teatro de Marion

Uma experiência narrativa e surreal ambientada em um teatro abandonado.

O projeto utiliza uma abordagem de aventura **point-and-click**, explorando narrativa visual, enigmas e elementos simbólicos.

**Acesso:** `demo/teatro_de_marion/`

### Yu-Gi-Oh! Forbidden Memories Remake

Projeto inspirado no clássico **Yu-Gi-Oh! Forbidden Memories**, desenvolvido com a proposta de recriar a experiência original utilizando uma abordagem moderna para a interface e os elementos visuais.

**Acesso:** `demo/yu_gi_oh_forbidden_memories_remake/`

---

## Funcionalidades

- Landing page para apresentação dos projetos
- Página de introdução com vídeo
- Controle de áudio da introdução
- Botão para pular a introdução
- Navegação responsiva
- Menu mobile com animações
- Sistema de partículas visuais
- Animações de entrada e scroll
- Cards interativos para os projetos
- Área dedicada às demos
- Seção de apoio aos projetos
- Links para redes sociais e suporte
- Interface otimizada para desktop e dispositivos móveis

---

## Tecnologias utilizadas

### Front-end

- **HTML5**
- **CSS3**
- **JavaScript**
- **GSAP**
- **ScrollTrigger**
- **Font Awesome**
- **SVG**

### Bibliotecas externas

O projeto utiliza bibliotecas carregadas via CDN:

- GSAP
- GSAP ScrollTrigger
- Font Awesome

---

## Estrutura do projeto

```text
xbrgames/
│
├── assets/
│   ├── 00000000.svg
│   ├── 00000001.svg
│   ├── 00000002.svg
│   ├── 00000003.svg
│   ├── 00000004.svg
│   └── 00000005.svg
│
├── demo/
│   ├── teatro_de_marion/
│   │   └── index.html
│   │
│   └── yu_gi_oh_forbidden_memories_remake/
│       └── index.html
│
├── intro/
│   └── intro.html
│
├── scripts/
│   └── script.js
│
├── styles/
│   └── style.css
│
└── index.html
```

---

## Arquitetura

O projeto foi estruturado separando responsabilidades entre **HTML, CSS e JavaScript**, evitando concentrar toda a aplicação em um único arquivo.

### HTML

Responsável pela estrutura e conteúdo das páginas:

- `index.html` — página principal
- `intro/intro.html` — apresentação inicial
- páginas localizadas dentro de `demo/` — execução dos projetos

### CSS

A estilização principal está centralizada em:

```text
styles/style.css
```

O arquivo contém:

- layout
- tipografia
- cores
- efeitos visuais
- cards
- navegação
- responsividade
- animações CSS
- estados de interação

### JavaScript

A lógica da página principal está em:

```text
scripts/script.js
```

O script controla principalmente:

- menu mobile
- partículas
- animações de entrada
- animações durante o scroll
- efeitos dos cards
- transições da interface

---

## Animações

Um dos principais elementos visuais do projeto é a utilização do **GSAP**.

As animações são utilizadas para criar uma apresentação mais dinâmica, incluindo:

- entrada da navbar
- animação da logo
- entrada do conteúdo principal
- animação das imagens dos projetos
- efeitos nos títulos
- animações dos cards
- efeitos durante o scroll
- animações da seção de apoio
- animações do footer

O **ScrollTrigger** é utilizado para disparar animações conforme os elementos entram na área visível da página.

Exemplo:

```javascript
gsap.from(".game-item img", {
    opacity: 0,
    scale: 0.3,
    rotation: 30,
    y: 50,
    duration: 1.5,
    ease: "elastic.out(1, 0.5)",
    scrollTrigger: {
        trigger: ".game-item img",
        start: "top 90%",
        toggleActions: "play none none none"
    }
});
```

---

## Introdução interativa

Antes de acessar a página principal, o projeto possui uma introdução em vídeo.

A página de introdução conta com:

- reprodução automática do vídeo
- carregamento com tela de loading
- controle de áudio
- botão para pular a introdução
- redirecionamento automático ao final do vídeo
- suporte a teclado

### Atalhos

| Tecla | Ação |
|---|---|
| `Espaço` | Ativar/desativar áudio |
| `S` | Pular introdução |

---

## Responsividade

A interface possui diferentes breakpoints para adaptar a experiência a diferentes tamanhos de tela.

Em dispositivos menores:

- a navegação é transformada em menu hamburger
- os cards passam para uma coluna
- elementos são redimensionados
- o conteúdo é reorganizado
- determinadas demos podem apresentar aviso de compatibilidade com desktop

A prioridade atual dos projetos de jogos é a experiência em **desktop**, especialmente para as demos que exigem maior área de interação.

---

## Como executar

Por utilizar tecnologias web nativas, o projeto não necessita de um processo de build complexo.

### 1. Clone o repositório

```bash
git clone https://github.com/JS171555/xbrgames.git
```

### 2. Entre no diretório

```bash
cd xbrgames
```

### 3. Execute

A página principal pode ser aberta diretamente no navegador:

```text
index.html
```

Para uma experiência mais consistente durante o desenvolvimento, recomenda-se utilizar um servidor local, como o **Live Server** do VS Code.

---

## Fluxo da aplicação

```text
Usuário
   │
   ▼
Introdução
   │
   ├── Pular
   │
   └── Finalizar vídeo
          │
          ▼
     Página XBRGAMES
          │
          ├── Projetos
          │      │
          │      ├── Teatro de Marion
          │      │
          │      └── Yu-Gi-Oh! Forbidden Memories Remake
          │
          ├── Apresentação
          │
          ├── Apoio aos projetos
          │
          └── Redes sociais / suporte
```

---

## Objetivos do projeto

O XBRGAMES foi desenvolvido com alguns objetivos principais:

- criar uma identidade visual própria para os projetos
- centralizar diferentes jogos em uma única plataforma
- apresentar os projetos de forma profissional
- explorar animações modernas para interfaces web
- desenvolver experiências interativas utilizando tecnologias web
- disponibilizar jogos diretamente pelo navegador
- criar uma base que possa receber novos projetos futuramente

---

## Próximos passos

Algumas evoluções planejadas para a plataforma incluem:

- [ ] Adicionar novos projetos
- [ ] Criar páginas individuais para cada jogo
- [ ] Melhorar o sistema de navegação entre projetos
- [ ] Adicionar screenshots e trailers individuais
- [ ] Criar sistema de categorias
- [ ] Adicionar informações detalhadas de cada jogo
- [ ] Melhorar suporte para dispositivos móveis
- [ ] Implementar sistema de atualizações dos projetos
- [ ] Adicionar novas experiências interativas
- [ ] Evoluir a identidade visual da plataforma

---

## Contribuição

Este projeto possui caráter independente e experimental, mas sugestões e contribuições são bem-vindas.

Para contribuir:

```bash
# Faça um fork do projeto

# Crie uma branch
git checkout -b feature/minha-feature

# Faça suas alterações
git add .
git commit -m "feat: adiciona nova funcionalidade"

# Envie sua branch
git push origin feature/minha-feature
```

Depois, abra um **Pull Request**.

---

## Licença

Este projeto possui finalidade independente e experimental.

Os códigos desenvolvidos neste repositório podem ser utilizados como referência para estudos e evolução do projeto, respeitando os direitos autorais de bibliotecas, assets, marcas e propriedades intelectuais de terceiros utilizadas nos projetos.

**Yu-Gi-Oh!** e seus respectivos elementos são propriedades de seus detentores de direitos. Este projeto não representa uma produção oficial da franquia.

---

## Autor

**Junior santos**

Desenvolvimento independente de experiências interativas para web.

---

<p align="center">
  Desenvolvido com HTML, CSS, JavaScript e GSAP.
</p>
