# Log de trabalho

Registro das sessões desta empresa. O modelo começa sem histórico de empresa.

Acrescentar uma entrada ao terminar cada sessão, sem apagar as anteriores. A skill salvar registra e compartilha o trabalho. Só confirmar salvamento quando main remota contiver o trabalho. Se não concluir, informar o que ficou preservado na sessão e a pendência.

Cada entrada contém data, pessoa ou pessoas, apoio de IA, trabalho realizado, links, resultado e pendências e fonte. A pessoa vem da identificação confirmada na sessão. Não depender de cadastro local permanente. Não deduzir um nome humano apenas pelo computador, login ou autoria Git.

## Modelo de entrada

Copiar os campos abaixo ao registrar a primeira sessão. Os campos representam uma estrutura para preencher, não uma sessão realizada.

```markdown
## AAAA-MM-DD: assunto

- **Quem trabalhou:** pessoa ou pessoas, com apoio da IA utilizada.
- **O que foi feito:** trabalho realizado e links para os arquivos.
- **Resultado e pendências:** conclusões, propostas e o que falta validar.
- **Fonte:** conversa, reunião ou documento utilizado.
```

## Sessões

Ainda não há sessões registradas.

## Manutenção do modelo

Registro da manutenção da estrutura pública, separado das sessões da empresa. Não representa trabalho ou configuração de um cliente.

### 14/10/2026: começo no Cloud e salvamento em main

- **Quem trabalhou:** Jéssica, com apoio do Codex.
- **Trabalho:** retirada da skill de início; atualização automática e leitura do contexto em [CLAUDE.md](CLAUDE.md); revisão de [salvar](.claude/skills/salvar/SKILL.md), [configurar-cerebro](.claude/skills/configurar-cerebro/SKILL.md), [regras gerais](AGENTS.md) e [guia](README.md). O trabalho da sessão tem main como destino final, inclusive quando a branch de trabalho tiver outro nome.
- **Resultado:** revisão implementada. Formato das duas skills validado e preparo e salvamento exercitados com Codex em uma base privada isolada, com conferência da main remota. Dois registros independentes foram combinados, preservando ambos, o índice e o log. Arquivos fora do pedido e ignorados ficaram fora do envio; uma cópia nova recuperou todos os registros. A manutenção do modelo não é uma configuração de empresa.
- **Pendências:** execução e descoberta automática das skills no Claude Cloud, uso por duas contas e conectores ainda não comprovados. Os ensaios de Git não substituem esse teste.
- **Fonte:** solicitação e revisão de Jéssica nesta sessão de 14/10/2026, arquivos do modelo e documentação oficial referenciada no README. Nenhum dado de cliente foi incluído.
