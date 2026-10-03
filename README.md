# anti-slop

Regras da Nettvo para impedir que sites feitos com IA saiam com os vícios de sempre:

1. Hierarquia falsa: todos os títulos enormes e o resto em letra pequena
2. Frases motivacionais e de reflexão para encher linguiça
3. Numeração decorativa ("01 Sobre", "02 Serviços")
4. Excesso de ícones (relógio, seta, coração)
5. Explicações que ninguém pediu ("Dados protegidos por acesso")
6. Fotos de banco sem vida
7. Informação em excesso ou duplicada entre seções

## Aviso de revisão humana

Toda resposta da IA que entrega ou altera um site termina com o bloco **REVISÃO HUMANA PENDENTE** (Passo 4 de `DESIGN_RULES.md`). Ele lista os dados que a IA escreveu sem confirmação, os placeholders a trocar e as conferências que só uma pessoa consegue fazer: hierarquia vista no navegador, qualidade das fotos, duplicação, teste em celular real e aprovação do cliente. Se o bloco não aparecer, a IA não seguiu as regras.

## Arquivos

| Arquivo | Para quê |
|---|---|
| `DESIGN_RULES.md` | As regras, que são a fonte da verdade |
| `EXAMPLES.md` | Pares proibido vs. correto para cada regra |
| `prompts/BOOTSTRAP.md` | Prompt curto para colar nas instruções do Projeto, Gem ou GPT |
| `prompts/AUDIT.md` | Prompt de auditoria para rodar num chat novo |
| `skills/anti-slop/SKILL.md` | Skill para Claude Code |
| `scripts/check.mjs` | Detector automático (Node, sem dependências) |

## Como usar

**Claude (claude.ai):** crie um Projeto e cole o bloco de `prompts/BOOTSTRAP.md` nas instruções. A busca na web precisa estar ativada para o chat conseguir ler os arquivos daqui.

**Claude Code:**
```bash
git clone https://github.com/nettvo/anti-slop ~/.claude/skills/anti-slop-repo
ln -s ~/.claude/skills/anti-slop-repo/skills/anti-slop ~/.claude/skills/anti-slop
```
No Windows (PowerShell):
```powershell
git clone https://github.com/nettvo/anti-slop "$HOME\.claude\skills\anti-slop-repo"
Copy-Item -LiteralPath "$HOME\.claude\skills\anti-slop-repo\skills\anti-slop" -Destination "$HOME\.claude\skills\anti-slop" -Recurse
```

**Cursor:** copie o conteúdo de `DESIGN_RULES.md` para `.cursor/rules/anti-slop.mdc`.

**Detector:**
```bash
node scripts/check.mjs src/
```
O comando sai com código 1 quando encontra erros, então serve para pre-commit ou CI.

## Manutenção

Viu um vício novo? Acrescente um par proibido/correto em `EXAMPLES.md`. Os exemplos corrigem a IA mais do que regras novas.
