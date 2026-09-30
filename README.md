# Guia do Challenge II

Guia semanal do Challenge II (Classical Conversations): para cada tarefa, os
passos com checklist e prompts para pedir ajuda à IA **sem que ela faça o
trabalho** (a IA pergunta, explica e corrige; quem pensa e escreve é o aluno).

Cada semana é uma página só, no mesmo formato do roteiro
(<https://github.com/Benranha/roteironananada>): HTML, CSS e JavaScript em um
único arquivo, sem dependências e sem build. Abrir o arquivo já funciona,
offline inclusive.

- `index.html` — Semana 22
- `semana-23.html` — Semana 23
- botões entre as semanas: menu do topo, pílulas na capa, botão no fim da
  página e no card de parabéns

## O que a página faz

- painéis por matéria, com blocos por dia e checkbox em cada passo
- prompts prontos com botão **Copiar**
- barra de progresso flutuante com porcentagem, marcos de 25/50/75% e um atalho
  por matéria; progresso por matéria no cabeçalho de cada painel
- aviso e confete a cada matéria fechada, e card de parabéns na semana inteira
- estado salvo no `localStorage` (por navegador), com botão de zerar; cada
  semana guarda o seu (`guia-s22`, `guia-s23`)
- tema claro e escuro, foco visível, respeita `prefers-reduced-motion` e
  esconde a barra na impressão

## Editar

O conteúdo está nos próprios HTMLs, em blocos `.bloco` dentro de cada
`<section class="dia">`. Cada caixinha tem um `data-k` fixo (`b1`, `m3`...):
é ele que identifica o progresso salvo, então **não renumere** ids existentes.
Ao criar uma semana nova, copie a última, troque a constante `CHAVE`, o número
da semana e os links de semana anterior/próxima nas duas pontas.

## No ar

<https://guia-challenge.vercel.app> (Semana 22) e
<https://guia-challenge.vercel.app/semana-23>. Página estática, sem build.
`vercel.json` liga `cleanUrls`. Se publicar por CLI, publique a pasta inteira:
sem o `index.html` a raiz dá 404.
