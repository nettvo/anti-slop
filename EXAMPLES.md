# Exemplos — proibido vs. correto

A IA segue exemplos melhor do que regras abstratas. Quando surgir um vício novo, acrescente um par aqui.

## 1. Hierarquia real

**Proibido**
```html
<h1 class="text-7xl">Advocacia com propósito</h1>
<h2 class="text-6xl">Nossos serviços</h2>
<h2 class="text-6xl">Sobre nós</h2>
<p class="text-sm">Atuamos em direito de família e sucessões há 15 anos.</p>
```
Os títulos de seção têm quase o tamanho do H1, e a informação útil está em letra pequena.

**Correto**
```html
<h1 class="text-5xl md:text-6xl font-semibold">Direito de família e sucessões em Curitiba</h1>
<p class="text-lg">15 anos resolvendo inventários, divórcios e guarda.</p>
<h2 class="text-3xl font-semibold">Áreas de atuação</h2>
<h3 class="text-base font-semibold">Inventário</h3>
```
O H1 diz o que a empresa faz e onde atua. O título de cada item tem o tamanho do corpo, em negrito.

## 2. Frase motivacional ou de reflexão

| Proibido | Correto |
|---|---|
| "Porque cada detalhe importa." | "Revisamos o contrato em até 48h." |
| "Transformando sonhos em realidade." | "Entregamos o site publicado em 3 semanas." |
| "Juntos, vamos mais longe." | *(cortar a frase)* |
| Citação de Steve Jobs no rodapé | *(cortar a citação)* |

Para decidir, pergunte se a frase informa, convence com um fato ou orienta uma ação. Se não fizer nenhuma das três, ela sai.

## 3. Numeração decorativa

**Proibido**
```
01 — Sobre
02 — Serviços
03 — Contato
```

**Correto**
```
Sobre
Serviços
Contato
```

Número só aparece quando a ordem importa:
```
Como funciona
1. Você envia os documentos
2. Analisamos em até 48h
3. Agendamos a reunião
```

## 4. Ícones

| Proibido | Correto |
|---|---|
| 🕐 Horário: seg a sex, 9h–18h | Seg a sex, 9h–18h |
| Saiba mais → (seta em todo link) | Saiba mais |
| ❤️ "Feito para você" | *(cortar)* |
| 📞 (11) 99999-9999 | (11) 99999-9999 |
| ✨ em título | *(cortar)* |

Ícone permitido: grade de 6 serviços equivalentes em que o ícone ajuda a escanear, ou controles de interface (menu, fechar, busca).

## 5. Explicações que ninguém pediu

| Proibido | Correto |
|---|---|
| "🔒 Dados protegidos por acesso" | *(cortar)* |
| "Site 100% seguro" | *(cortar)* |
| "Suas informações estão protegidas conosco" abaixo do newsletter | *(cortar)* |
| — | "O orçamento é gratuito e sem compromisso", ao lado do botão de orçamento (resolve uma dúvida real no ponto de decisão) |

## 6. Imagens

**Proibido**
- Pessoa de terno sorrindo para a câmera com fundo branco
- Aperto de mão corporativo
- Quatro pessoas olhando juntas para um notebook
- Rosto com olhar vazio, iluminação de estúdio

**Correto**
- Foto real do cliente ou da equipe trabalhando
- Sem foto real, um placeholder descritivo:
```html
<div class="aspect-[4/3] bg-neutral-200 grid place-items-center text-neutral-600 text-sm p-6 text-center">
  [Foto: advogada explicando documento a um casal na mesa do escritório, luz natural]
</div>
```

## 7. Duplicação e excesso

**Proibido**
- Hero: "Atendemos em todo o Brasil, online e presencial"
- Seção Sobre: "Nosso atendimento cobre todo o país, online ou presencial"
- Seção Diferenciais: "Atendimento online e presencial em todo o Brasil"

**Correto**
- A informação aparece uma vez só, na seção que é dona dela (aqui, o Hero). As outras seções tratam de outro assunto ou deixam de existir.
- Exceção: telefone, e-mail e endereço podem se repetir no rodapé.

## Aviso de revisão humana (Passo 4)

**Proibido**
> Lembre-se de revisar o site antes de publicar!

Genérico, sem nenhum item real. Ninguém age a partir disso.

**Correto**
> **REVISÃO HUMANA PENDENTE — o site não está pronto para publicar até isto ser conferido**
>
> **A. Dados que escrevi sem confirmação**
> - [Hero] "15 anos de atuação" → confirmar com o cliente
> - [Contato] telefone (41) 3333-0000 e horário seg–sex 9h–18h → confirmar
>
> **B. Placeholders a substituir**
> - [Sobre] foto da advogada no escritório
> - [Rodapé] link do Instagram
>
> **C. Conferências que só uma pessoa faz**
> - [ ] Hierarquia em escala de cinza no navegador
> - [ ] Fotos finais com pessoas reais em ação
> - [ ] Duplicação: ler o site inteiro
> - [ ] Teste em celular real
> - [ ] Textos aprovados pelo cliente
>
> **D. Detector automático**
> - 0 erros, 1 aviso (imagem de banco na seção Áreas)
