# 🕹️ RETRO BATTLE CHAMPIONSHIP 2026

> Landing page interativa para um campeonato de e-sports com tema retrowave / pixel art.

![Status](https://img.shields.io/badge/status-finalizado-brightgreen) ![Front-end](https://img.shields.io/badge/front--end-HTML%2FCSS%2FJS-blue)

---

## 📋 Análise do Código

Este código cria uma página web completa para um campeonato de jogos eletrônicos fictício chamado **RETRO BATTLE CHAMPIONSHIP 2026**. Abaixo está uma análise detalhada de tudo o que ele faz, desde a estrutura visual até as interações dinâmicas.

---

## 🎨 1. Estrutura e Estilo Visual (Retrowave / Pixel Art)

- **Tema retrô / arcade**: utiliza fontes como `'Press Start 2P'` (estilo pixelado) e `'VT323'` (monoespaçada), fundo escuro com textura de linhas de scan, bordas grossas e sombras que imitam pixels.
- **Cores neon**: rosa (`#ff5eff`), ciano (`#00f0ff`), amarelo (`#ffe030`), verde (`#3cff3c`), vermelho e dourado.
- **Efeitos**:
  - Gradientes de fundo e sobreposição de scanlines (linhas horizontais animadas).
  - Brilho (`text-shadow`, `box-shadow`) e animações de pulsação em elementos como o distintivo, a data e os medalhões do pódio.
  - Cards interativos que se elevam e ganham cores de destaque ao passar o mouse.
- **Responsividade**: o layout se ajusta para tablets e celulares com `@media queries`, reduzindo tamanhos de fonte, espaçamentos e dimensões do pódio.

---

## 🚀 2. Cabeçalho Principal (Hero)

- Exibe o nome do evento com efeitos de neon.
- Um subtítulo descrevendo o campeonato.
- Data fixa: **15 de agosto de 2026**.
- Um selo animado “TORNEIO OFICIAL”.

---

## ⏳ 3. Contagem Regressiva

- Calcula em tempo real a diferença entre a data/hora atual e **15/08/2026 às 09:00 (horário de Brasília)**.
- Mostra dias, horas, minutos e segundos restantes.
- Atualiza a cada segundo via `setInterval`.
- Se a data já tiver passado, exibe zeros.

---

## 🎮 4. Seção “Jogos da Competição”

Quatro jogos em cards:
- **CS2** (Counter-Strike 2)
- **Valorant**
- **Overwatch 2**
- **Mortal Kombat 1**

Cada card possui uma imagem ilustrativa (buscada de URLs externas) e o nome do jogo. Ao passar o mouse, o card ganha uma cor de destaque específica para cada jogo (ex: laranja para CS2, vermelho para Valorant) e uma leve elevação.

---

## 🏆 5. Seção “Premiações” com Pódio

- Representação visual de um pódio com três lugares:
  - **1º lugar**: R$ 5.000 + Troféu + Kit Gamer (pilastra mais alta, dourada)
  - **2º lugar**: R$ 2.000 + Mouse Gamer (pilastra prata)
  - **3º lugar**: R$ 1.000 + Headset (pilastra bronze)
- Emojis de medalhas flutuam com animação.
- Ao passar o mouse sobre cada bloco do pódio, ele sobe ligeiramente.

---

## 📝 6. Formulário de Inscrição

- Campos obrigatórios:
  - Nome completo (mínimo 3 caracteres)
  - E-mail (validação de formato básico com regex)
  - Jogo escolhido (select com 4 opções)
  - Login (mínimo 4 caracteres)
  - Senha (mínimo 6 caracteres)
- **Validação front-end**:
  - Se algum campo estiver inválido, exibe um toast (notificação flutuante) com erro e foca no campo problemático.
  - Se todos os dados forem válidos, mostra um toast de sucesso com o nome do inscrito e o jogo escolhido.
  - Após o sucesso, o formulário é resetado e partículas animadas (estrelas, ícones de game) surgem na tela.
- **Importante**: o formulário **não envia dados para nenhum servidor** – é apenas uma simulação de cadastro (front-end puro).

---

## ✨ 7. Componentes Interativos Extras

- **Toast notifications**: aparece no topo central com mensagens de erro ou sucesso, desaparece após 4 segundos.
- **Partículas (spawnParticles)**: ao inscrever-se com sucesso, 30 pequenos ícones (⭐, ✨, 🎮, 🏆, etc.) sobem pela tela com animação, simulando confetes.
- **Navegação suave**: links internos âncora (embora não existam links visíveis, o código trata cliques em qualquer `<a href="#...">` para rolar suavemente até a seção correspondente).
- **Console logs** estilizados: ao abrir as ferramentas do desenvolvedor, o código exibe mensagens coloridas de boas-vindas.

---

## 🦶 8. Rodapé

- Informações de direitos autorais e um pequeno texto “FEITO COM ❤️ E PIXEL ART”.

---

## 🛠️ 9. Comportamentos Técnicos Não Óbvios

- **Imagens dos jogos**: são carregadas de URLs externas (DuckDuckGo). Caso alguma imagem esteja offline, o navegador mostrará o texto alternativo vazio, mas a estrutura permanece.
- **Estilos dinâmicos via atributo `data-game`**: cada card de jogo tem uma cor de destaque definida por variáveis CSS customizadas (`--accent`, `--accent-glow`), ativadas no hover.
- **Acessibilidade**: não há foco explícito em leitores de tela, mas os controles são utilizáveis via teclado (formulário, selects).
- **Pixel perfect**: o código força `image-rendering: crisp-edges` e `pixelated` para manter a estética retrô nas imagens.

---

## ❌ Resumo do que o código NÃO faz (para evitar mal-entendidos)

- Não envia dados para backend – é puramente uma demonstração visual.
- Não armazena inscrições em localStorage ou cookie.
- Não autentica usuário – a senha e login são apenas validados quanto ao comprimento.
- Não possui lógica de sorteio ou bracket de torneio.

Em essência, este código é uma **landing page interativa e estilizada** para divulgar um campeonato de e-sports, com contagem regressiva, apresentação de jogos, premiações e um formulário de pré-cadastro simulado.

---

## ▶️ Como executar

1. Copie todo o código HTML/CSS/JS para um arquivo `.html`.
2. Abra o arquivo em qualquer navegador moderno.
3. Não é necessário servidor ou internet (exceto para carregar as imagens externas e as fontes do Google Fonts).

---

## 📚 Conceitos abordados

- HTML5 semântico
- CSS3 com animações, flexbox, grid e responsividade
- JavaScript puro (manipulação do DOM, eventos, `setInterval`, validação de formulários, geração dinâmica de elementos)

