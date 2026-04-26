# Frontend Mentor - Bento Grid Solution

Esta é a minha solução para o desafio [Bento grid do Frontend Mentor](https://www.frontendmentor.io/challenges/bento-grid-RMydElrlOj). Os desafios do Frontend Mentor ajudam a melhorar as habilidades de desenvolvimento front-end através da construção de projetos realistas.

## Índice

- [Visão Geral](#visão-geral)
  - [O desafio](#o-desafio)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [Meu processo](#meu-processo)
  - [Tecnologias utilizadas](#tecnologias-utilizadas)
  - [O que eu aprendi](#o-que-eu-aprendi)

## Visão Geral

### O desafio

Os usuários devem ser capazes de:

- Visualizar o layout ideal para a interface, adaptando-se perfeitamente desde telas de dispositivos móveis até desktops.

### Screenshot

![Preview do projeto Bento Grid](./assets/img-tela.png)

### Links

- URL do Repositório: [https://github.com/SuellenMMarques/bentogrid]
- URL do Site (Live): [https://suellenmmarques.github.io/bentogrid/]

## Meu processo

### Tecnologias utilizadas

- HTML5 Semântico
- Variáveis CSS (Custom Properties) para paleta de cores e espaçamentos
- CSS Flexbox
- CSS Grid
- Fluxo de trabalho Mobile-first (Responsividade)

### O que eu aprendi

Este projeto foi um marco excelente para consolidar a transição de mentalidade entre o uso de **CSS Grid** e **Flexbox** em um cenário real e assimétrico (estilo Bento). 

O maior desafio prático foi gerenciar o posicionamento de múltiplos cartões que precisavam ocupar o mesmo espaço de coluna, mas em linhas diferentes, sem quebrar a responsividade. A principal lição técnica que aplico agora é a criação de "sub-colunas" através de `divs` conteineres (como a classe `.exception-column-container` no projeto). Ao invés de forçar o posicionamento com margens rígidas, deleguei o controle de alinhamento interno ao Flexbox e deixei o Grid responsável apenas pelo esqueleto principal da página, aproveitando o poder do `1fr` para uma distribuição fluida.

```css
/* Exemplo de solução para a coluna de exceção no Grid */
.exception-column-container {
    grid-column: 1 / 2;
    grid-row: 1 / -1;
    flex-direction: column;
    height: 100%;
}

