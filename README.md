# Segundo cérebro da empresa

Uma base em arquivos para guardar contexto, processos e conhecimento do trabalho. O Claude Code consulta e atualiza esses arquivos; o GitHub guarda as versões compartilhadas.

Este é um **modelo público da LÍNIA Consultoria**. Crie uma base privada própria para sua empresa antes de trabalhar. As pessoas da mesma empresa usam essa mesma base, cada uma com sua conta e sua pasta no computador.

## Estrutura

```text
empresa-OS/
  README.md
  identidade.md
  AGENTS.md
  CLAUDE.md
  LOG.md
  .gitignore
  clientes/
    README.md
  processos/
    README.md
  .claude/
    skills/
      cerebro/
        SKILL.md
      salvar/
        SKILL.md
```

Um cliente real ganha `clientes/<nome-do-cliente>/README.md` quando houver conteúdo. Não há clientes de exemplo para serem confundidos com clientes reais.

| Local | O que guardar |
|---|---|
| [identidade.md](identidade.md) | Quem é a empresa e como decide, escreve e trabalha. |
| [clientes/](clientes/README.md) | Contexto, fontes e particularidades de cada cliente. |
| [processos/](processos/README.md) | Como o trabalho é feito, com critérios, fontes e estágio de validação. |
| [LOG.md](LOG.md) | Registro das sessões: data, autoria, trabalho, resultado e pendências. |
| [AGENTS.md](AGENTS.md) | Orientações gerais para a IA. O CLAUDE.md importa essas regras. |
| [.claude/skills/](.claude/skills/cerebro/SKILL.md) | As rotinas cerebro e salvar. |

## 1. Criar a base da empresa

1. Cada pessoa cria sua própria conta no [GitHub](https://github.com/signup).
2. Abra o [repositório modelo](https://github.com/jesilveiraa/segundo-cerebro-modelo).
3. Clique em **Use this template > Create a new repository**.
4. Escolha quem será proprietário: uma conta de uma das pessoas ou uma organização da empresa. Use um nome como `cerebro-da-empresa` e selecione **Private**.
5. Clique em **Create repository from template**. Crie uma única base para a empresa.
6. Se usou uma conta pessoal, abra **Settings > Collaborators > Add people** e convide a outra pessoa. Ela precisa aceitar o convite com a conta dela. Em uma organização, conceda acesso de escrita às pessoas que vão trabalhar na base.
7. Copie o link da base que acabou de criar. Esse é o link que as duas vão usar, não o link deste modelo público.

A cópia da empresa tem vida própria. Mudanças futuras neste modelo não substituem automaticamente seus arquivos.

## 2. Trazer a base para cada computador

Use o **Claude Code em ambiente local**, com acesso aos arquivos e à execução de comandos. Uma conversa comum sem acesso ao computador não consegue fazer esta etapa.

Abra uma pasta de trabalho no Claude Code. Escolha o destino da base fora de pastas sincronizadas por OneDrive, iCloud ou Dropbox. Use o prompt abaixo, preenchendo os três campos. No segundo computador, repita com o mesmo repositório da empresa e o destino local dessa pessoa.

### Prompt para copiar a base

```text
Quero trazer o cérebro da minha empresa para este computador.

Repositório da empresa: <LINK_DO_REPOSITORIO_PRIVADO_DA_EMPRESA>
Pasta de destino: <CAMINHO_COMPLETO_DA_PASTA_NO_MEU_COMPUTADOR>
Quem está trabalhando: <MEU_NOME>

Confira se você tem acesso local aos arquivos e à execução de comandos.
Confira o Git e o acesso ao GitHub para receber e enviar atualizações.
Se faltar uma ferramenta ou acesso, explique o necessário e me guie na
configuração pelo fluxo oficial. Não peça senha ou token nesta conversa.
Configure apenas o necessário para esta base, sem alterar outros projetos.

Confira a pasta de destino. Preserve qualquer conteúdo existente.
Se já for a base indicada, reutilize-a; se houver outro conteúdo,
explique a situação antes de mudar o destino. Não sobrescreva arquivos.

Clone o repositório privado da empresa para a pasta de destino.
Confirme que o destino de sincronização é essa base, e não o modelo público
jesilveiraa/segundo-cerebro-modelo. Não crie outra base no GitHub.

Leia README.md, AGENTS.md e CLAUDE.md. Confira as skills cerebro e salvar.
Informe qual pasta devo abrir no Claude Code para usá-las.
Pergunte somente as informações necessárias para preencher identidade.md.
Não invente dados da empresa nem cadastre clientes fictícios.

Registre a configuração no LOG.md com meu nome, data, resultado e fonte.
Use a rotina salvar para compartilhar os registros dessa configuração.
Confira o recebimento e envio e diga o que foi comprovado e o que falta.
Se as skills ainda não aparecerem nesta conversa, abra uma nova sessão
na pasta clonada ou leia seus SKILL.md e siga as rotinas diretamente.
```

O Git e a autenticação precisam estar disponíveis em cada computador. Siga as telas oficiais de acesso quando solicitado. As skills orientam a rotina, mas não substituem essas permissões.

## 3. Primeiro uso

1. Abra a pasta criada no Claude Code.
2. Use `/cerebro` e diga seu nome e o assunto em que quer trabalhar. Exemplo: `/cerebro vamos registrar como preparamos reuniões`.
3. Preencha a identidade com informações reais. Cadastre clientes apenas quando houver contexto para guardar.
4. Trabalhe com a IA e confira os arquivos usados como fonte.
5. Ao terminar, use `/salvar`.
6. Confira a resposta: quais arquivos foram salvos, se o envio foi confirmado e quais pendências ficaram.

Teste a troca com outra pessoa: uma altera um critério em um arquivo e usa salvar; a outra usa cerebro e mostra a alteração recebida. Depois façam o caminho de volta.

## Rotina

- **cerebro:** recebe atualizações e lê o contexto relevante para começar.
- **salvar:** atualiza os registros nos lugares certos, acrescenta a sessão ao log e compartilha as alterações.

Salvar no computador não garante que o conteúdo chegou à outra pessoa. Se faltar internet ou acesso, a IA deve dizer o que ficou local. Se as duas alterarem o mesmo conteúdo, a rotina compara as versões e pede ajuda somente quando houver uma decisão de significado em aberto.

As skills também podem ser usadas por um pedido claro, como “atualize o cérebro antes de começarmos” ou “salve e compartilhe o trabalho desta sessão”.

## Fontes e conexões da empresa

Preencher com as fontes realmente escolhidas. Não guardar credenciais.

| Fonte ou ferramenta | O que contém | Link ou localização | Acesso e teste |
|---|---|---|---|
| A definir | A definir | A definir | Não configurado |

Tarefas atuais, agenda, bases operacionais e gravações continuam no sistema de origem. Registrar aqui o link e o papel de cada fonte. Fontes específicas de um cliente ficam no README dele.

As conexões com ferramentas são feitas pelos **Conectores** do próprio Claude. Cada pessoa usa seu acesso e confere a consulta no ambiente em que trabalha. Conectar uma ferramenta não agenda uma automação.

## Sobre este modelo

Versão inicial de 11/10/2026, criada para a mentoria de segundo cérebro e IA da LÍNIA. As rotinas devem ser verificadas nos computadores das pessoas que vão utilizá-las. Não instalam agendadores nem enviam mensagens ou publicam materiais para clientes.

Referências: [modelo no GitHub](https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-repository-from-a-template), [cópia local](https://docs.github.com/en/repositories/creating-and-managing-repositories/cloning-a-repository), [Claude Code local](https://code.claude.com/docs/en/desktop), [skills do Claude Code](https://code.claude.com/docs/en/skills) e [Conectores](https://support.claude.com/en/articles/11176164-use-connectors-to-extend-claude-s-capabilities).
