# Log de trabalho

**As sessões desta empresa ficam em [log/](log/README.md), um arquivo por sessão.** Este arquivo guarda a regra de registro e a manutenção do modelo. O modelo começa sem histórico de empresa.

Cada sessão cria o seu próprio arquivo em `log/AAAA-MM-DD-assunto.md`, sem apagar ou editar os das outras. A skill salvar registra e compartilha o trabalho. Só confirmar salvamento quando main remota contiver o trabalho. Se não concluir, informar o que ficou preservado na sessão e a pendência.

Cada registro contém data, pessoa ou pessoas, apoio de IA, trabalho realizado, links, resultado e pendências e fonte. A pessoa vem da identificação confirmada na sessão. Não depender de cadastro local permanente. Não deduzir um nome humano apenas pelo computador, login ou autoria Git.

**Por que um arquivo por sessão:** quando todas as sessões escrevem no fim do mesmo arquivo, duas sessões simultâneas disputam as mesmas linhas e alguém precisa resolver o conflito. Com um arquivo por sessão, o Git combina sozinho. Pelo mesmo motivo, não manter um índice que cada sessão precise atualizar: a pasta ordenada por data já serve de índice, e um sumário é gerado quando alguém pedir.

**Base criada antes desta mudança:** preservar o histórico já existente neste arquivo e começar o formato novo a partir da data da adoção, sem reescrever registros antigos.

## Manutenção do modelo

Registro da manutenção da estrutura pública, separado das sessões da empresa. Não representa trabalho ou configuração de um cliente.

### 14/10/2026: começo no Cloud e salvamento em main

- **Quem trabalhou:** Jéssica, com apoio do Codex.
- **Trabalho:** retirada da skill de início; atualização automática e leitura do contexto em [CLAUDE.md](CLAUDE.md); revisão de [salvar](.claude/skills/salvar/SKILL.md), [configurar-cerebro](.claude/skills/configurar-cerebro/SKILL.md), [regras gerais](AGENTS.md) e [guia](README.md). O trabalho da sessão tem main como destino final, inclusive quando a branch de trabalho tiver outro nome.
- **Resultado:** revisão implementada. Formato das duas skills validado e preparo e salvamento exercitados com Codex em uma base privada isolada, com conferência da main remota. Dois registros independentes foram combinados, preservando ambos, o índice e o log. Arquivos fora do pedido e ignorados ficaram fora do envio; uma cópia nova recuperou todos os registros. A manutenção do modelo não é uma configuração de empresa.
- **Pendências:** execução e descoberta automática das skills no Claude Cloud, uso por duas contas e conectores ainda não comprovados. Os ensaios de Git não substituem esse teste.
- **Fonte:** solicitação e revisão de Jéssica nesta sessão de 14/10/2026, arquivos do modelo e documentação oficial referenciada no README. Nenhum dado de cliente foi incluído.

### 14/10/2026: conferência do entendimento e registro seletivo

- **Quem trabalhou:** Jéssica, com apoio do Codex.
- **Trabalho:** acrescentada conferência curta do entendimento, fontes e lacunas em [configurar-cerebro](.claude/skills/configurar-cerebro/SKILL.md). Detalhados seleção, destinos, duplicações, correções e pontos sem fonte operacional em [salvar](.claude/skills/salvar/SKILL.md). Prompt de continuação apenas sob pedido, sem emissão ou pergunta automática ao salvar. [Guia](README.md) alinhado às instruções.
- **Resultado:** instruções ajustadas sem mudar a organização da base ou o fluxo de conclusão em main. Não criado arquivo de pendências ou controle de tarefas. Não incluídos dados de empresa ou cliente. Formato e coerência dos arquivos conferidos; não executado novo ensaio de recuperação.
- **Pendências:** aplicação das novas orientações no Claude Cloud não comprovada. A conferência do entendimento não equivale a validar procedimentos da empresa. Uma possível lista de pendências exige estudo, teste e pedido de implementação próprios.
- **Fonte:** revisão de Jéssica nesta conversa em 14/10/2026 e confirmação de configurar-cerebro como skill de preparação da base. Esta é manutenção do modelo, não sessão de uma empresa.

### 17/10/2026: contexto por áreas e mapa dos processos

- **Quem trabalhou:** Jéssica, com apoio do Codex.
- **Trabalho:** identidade movida para [contexto-da-empresa/identidade.md](contexto-da-empresa/identidade.md), junto dos pontos de partida de ofertas, clientes e mercado, pessoas e comunicação. Entrada de processos renomeada para [mapa-dos-processos.md](processos/mapa-dos-processos.md), com jornada, back office e rotinas em nível macro. Alinhados README, CLAUDE e caminhos das duas skills.
- **Resultado:** [AGENTS.md](AGENTS.md) atribui à IA a organização, a referência principal, o registro de fontes e datas disponíveis e a atualização com preservação do histórico. As pessoas fornecem materiais, esclarecem lacunas e revisam. Preenchimento gradual e criação de arquivos adicionais só com conteúdo e necessidade. Modelo permanece genérico, sem dados de empresa ou cliente.
- **Conferência e limites:** links locais, caminhos e diferenças revisados; formato das duas skills aprovado pelo validador. Não executado novo ensaio de uso no Claude Cloud. Bases privadas já criadas não foram alteradas nem recebem esta revisão automaticamente.
- **Fonte:** pedido explícito de Jéssica em 17/10/2026 para revisar a organização e as instruções do modelo, a partir dos comentários no material de apoio da aula Contexto da empresa. Registro de manutenção separado das sessões de uma empresa.

### 13/11/2026: salvamento no Cloud, publicação por etapa e log por sessão

- **Quem trabalhou:** Jéssica, com apoio do Claude Code (Opus 5).
- **Por que:** na primeira base criada a partir deste modelo, 15 sessões entre 23/10 e 12/11/2026 registraram o trabalho e não concluíram o envio para main, sem que nada avisasse. No Claude Code em Cloud a branch da sessão é descartável, então o que não chega a main se perde quando a sessão termina. O log único era tocado em 184 de 266 commits daquela base, o que o tornava o ponto de disputa entre sessões simultâneas.
- **Trabalho:** em [AGENTS.md](AGENTS.md) e [CLAUDE.md](CLAUDE.md), o pedido de trabalho passou a autorizar o envio a cada etapa concluída e revisada, sem esperar um pedido de salvamento no fim, e toda resposta que alterar arquivos passou a terminar com uma linha informando se o envio aconteceu. Em [salvar](.claude/skills/salvar/SKILL.md), o passo 6 repete receber, combinar e reenviar até cinco vezes quando a recusa for apenas de concorrência, em vez de encerrar após uma tentativa, e o registro da sessão passou a ser um arquivo próprio em [log/](log/README.md). Estrutura e mapa do [guia](README.md) atualizados.
- **Resultado:** quatro ajustes aplicados no modelo. As mudanças de publicação, nova tentativa e linha de situação também foram aplicadas na base da primeira empresa, a pedido dela; o formato de log por sessão ficou apenas no modelo, para bases novas, para não exigir migração de uma base em uso.
- **Pendências:** comportamento não testado com duas sessões simultâneas. A recuperação do conteúdo que ficou em branches de sessão naquela base continua pendente. Bases privadas já criadas não recebem esta revisão automaticamente.
- **Fonte:** análise dos repositórios em 13/11/2026 e decisões de Jéssica nesta conversa. Manutenção do modelo, sem dados de empresa ou cliente.
