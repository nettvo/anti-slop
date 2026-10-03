# REGRAS DE CONSTRUÇÃO DE SITES — LEITURA OBRIGATÓRIA ANTES DE QUALQUER CÓDIGO

Este arquivo é a fonte da verdade. Exemplos de proibido vs. correto para cada regra: [EXAMPLES.md](./EXAMPLES.md).

## Passo 1 — Mapa de conteúdo (antes do layout)
Monte uma tabela: seção → objetivo da seção → informações que ela contém.
Cada informação aparece em UMA seção só. Se um dado aparece em duas, decida qual
seção é a dona e tire da outra (ou troque por um link).
Toda seção precisa responder: "o que o visitante decide ou faz depois de ler isto?".
Se não houver resposta, a seção sai.

## Passo 2 — Regras

### 1. Hierarquia real
- Se todo título é grande, nenhum título é importante. Tamanho é recurso escasso.
- Um único H1 por página. Só um elemento em tamanho de destaque por tela visível.
- Escala fixa e consistente (ex.: H1 ~3rem · H2 ~2rem · H3 ~1.25rem · corpo 1–1.125rem).
  No celular o H1 cai para ~2–2.25rem.
- Use peso, cor e espaçamento para hierarquia, não só tamanho. Título de seção
  secundária pode ter o mesmo tamanho do corpo, em negrito.
- O corpo do texto NUNCA abaixo de 16px. Texto pequeno fica restrito a legendas e notas legais.
- Teste: em escala de cinza e com zoom reduzido, deve dar para identificar em
  2 segundos a coisa mais importante de cada tela.

### 2. Zero frase motivacional ou de reflexão
- Proibido: frases inspiracionais, citações, "porque cada detalhe importa",
  "transformando sonhos em realidade", fechamentos poéticos de seção.
- Toda frase precisa INFORMAR, CONVENCER com um fato concreto ou ORIENTAR uma ação.
  Se não faz nenhuma das três, é cortada.
- Prefira o específico ao genérico: "Atendimento em até 24h úteis" em vez de
  "Estamos sempre ao seu lado".

### 3. Sem numeração decorativa
- Proibido: "01 / Sobre", "02 / Serviços", números grandes antes de títulos de seção,
  listas numeradas de itens que não têm ordem.
- Número só é usado quando a ORDEM importa de verdade (passo a passo de um processo)
  ou quando é um dado real (preço, prazo, quantidade).

### 4. Ícones só quando trabalham
- Ícone só entra se ajuda a escanear uma lista de itens equivalentes (ex.: grade de
  serviços) OU substitui texto num controle de interface conhecido (menu, fechar, busca).
- Proibido: ícone repetindo o que o texto já diz (relógio ao lado de "Horário",
  seta ao lado de todo link, telefone ao lado de um número já evidente).
- Proibido: corações, estrelas e brilhos decorativos. Emoji como ícone, nunca.
- Na dúvida, sem ícone.

### 5. Nada de explicação que o cliente não pediu
- Proibido microtexto defensivo ou técnico não solicitado: "Dados protegidos por acesso",
  "Site seguro", "Suas informações estão protegidas", "Feito com carinho",
  selos genéricos de confiança.
- Só escreva algo assim se o cliente pediu OU se resolve uma dúvida real exatamente no
  ponto de decisão (ex.: "Não cobramos nada para o orçamento" ao lado do formulário
  de orçamento).

### 6. Imagens com vida
- Prioridade: fotos reais do cliente > placeholder descritivo > banco de imagens.
- Se não houver foto real, use um placeholder com legenda do que a foto deve mostrar
  (ex.: "[Foto: advogada atendendo cliente na mesa, luz natural]") em vez de stock genérico.
- Se usar banco de imagens: pessoas em ação, olhando para a tarefa ou umas para as outras,
  contexto real, luz natural. Proibido: pessoas sorrindo para a câmera sem motivo,
  aperto de mão corporativo, grupo olhando para um notebook, olhar vazio.
- Toda imagem precisa mostrar algo que o texto não diz sozinho.

### 7. Densidade e duplicação
- Cada seção tem uma ideia principal e no máximo 3 pontos de apoio.
- Proibido repetir o mesmo dado em seções diferentes (endereço, telefone, lista de
  serviços, diferenciais). O rodapé pode repetir contato; o resto, não.
- Se o hero já disse, a seção seguinte não repete com outras palavras.

## Passo 3 — Auditoria antes de entregar
Antes de mostrar o resultado, revise o próprio código contra a lista abaixo e corrija
o que falhar. Depois informe em no máximo 5 linhas o que foi corrigido.

[ ] Só um H1 e só um destaque tipográfico por tela
[ ] Nenhuma frase motivacional, citação ou fechamento poético
[ ] Nenhum número decorativo em seção ou lista sem ordem
[ ] Todo ícone passa no teste "trabalha ou sai"
[ ] Nenhum microtexto defensivo não solicitado
[ ] Nenhuma imagem stock genérica; placeholders descritivos quando faltar foto real
[ ] Nenhum dado aparece em duas seções (exceto contato no rodapé)
[ ] Corpo de texto ≥ 16px e hierarquia legível em escala de cinza

## Passo 4 — Aviso de revisão humana (obrigatório no fim da resposta)
Toda resposta que entrega ou altera um site termina com o bloco abaixo, sempre por último,
depois do resumo da auditoria. Ele existe porque parte destas regras não pode ser verificada
por quem só escreveu o código.

Regras do bloco:
- Nunca omitir, nunca resumir em uma frase ("revise o site antes de publicar" é proibido).
- As listas A e B citam itens REAIS deste site, com a seção onde estão. Se não houver nenhum, escreva "nenhum".
- A lista C aparece sempre e inteira, porque a IA não consegue fazer essas conferências.
- Em alterações posteriores, repita o bloco mostrando só o que continua pendente e o que a alteração criou.

Formato exato:

---
**REVISÃO HUMANA PENDENTE — o site não está pronto para publicar até isto ser conferido**

**A. Dados que escrevi sem confirmação** (preços, telefones, endereços, horários, prazos, números, nomes, cargos)
- [seção] dado → confirmar com o cliente

**B. Placeholders a substituir**
- [seção] o que falta (foto, logo, texto, link)

**C. Conferências que só uma pessoa faz**
- [ ] Hierarquia: abrir no navegador em escala de cinza (DevTools → Rendering → Emulate vision deficiencies → Achromatopsia) e com zoom afastado. A informação mais importante de cada tela se destaca em 2 segundos?
- [ ] Fotos: as imagens finais mostram pessoas reais em ação, com olhar vivo, e acrescentam algo que o texto não diz?
- [ ] Duplicação: ler o site inteiro de cima a baixo. Alguma informação aparece em mais de uma seção?
- [ ] Celular: abrir num aparelho de verdade, não só no modo responsivo do navegador.
- [ ] Aprovação: o cliente leu e aprovou os textos?

**D. Detector automático**
- Resultado de `node scripts/check.mjs`, ou "não executado: rode antes de publicar".
---
