# Log de trabalho: um arquivo por sessão

Cada sessão de trabalho nesta base cria aqui o seu próprio arquivo, com o nome `AAAA-MM-DD-assunto.md`. Exemplo: `2026-11-17-contexto-dos-servicos.md`.

Uma sessão não edita o arquivo de outra. Se duas pessoas trabalharem ao mesmo tempo, cada uma escreve no seu arquivo e o Git combina os dois sozinho, sem ninguém precisar resolver conflito.

Esta pasta não tem índice atualizado a cada sessão, de propósito: um índice assim voltaria a ser o arquivo que todas as sessões disputam. Os nomes começam pela data, então a própria ordenação da pasta já mostra o histórico. Um sumário pode ser gerado quando alguém pedir.

## Estrutura de cada arquivo

```markdown
# AAAA-MM-DD: assunto

- **Quem trabalhou:** pessoa ou pessoas, com apoio da IA utilizada.
- **O que foi feito:** trabalho realizado e links para os arquivos.
- **Resultado e pendências:** conclusões, propostas e o que falta validar.
- **Fonte:** conversa, reunião ou documento utilizado.
```

Os campos acima são uma estrutura para preencher, não uma sessão realizada. Toda sessão recebe registro, inclusive quando resultar apenas em análise ou revisão. A regra completa está em [AGENTS.md](../AGENTS.md), seção Encerrar.

O registro aponta o trabalho feito. Decisões, tarefas e conhecimento da empresa ficam em suas próprias fontes, com links a partir daqui.
