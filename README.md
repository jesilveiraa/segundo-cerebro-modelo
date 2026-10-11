# Segundo cérebro da empresa

Uma base em arquivos para guardar contexto, processos e conhecimento do trabalho. O Claude Code consulta e atualiza esses arquivos; o GitHub guarda as versões compartilhadas.

Este é um **modelo público da LÍNIA Consultoria**. Crie uma base privada própria para sua empresa antes de trabalhar. As pessoas da mesma empresa usam essa mesma base, cada uma com sua conta e sua pasta no computador.

## Por onde começar

| Sua situação | Comece aqui |
|---|---|
| A empresa ainda não tem uma base | Crie uma única base pela etapa 1. Depois siga as etapas 2 e 3. |
| Outra pessoa já criou a base da empresa | Aceite o convite de acesso e use o link dessa base. Comece na etapa 2, sem criar outro repositório. |
| A base já está configurada neste computador | Vá direto à etapa 4: cerebro, trabalho e salvar. |

Antes da cópia, abra o Claude no modo **Code**, em ambiente local, e entre com uma conta que tenha acesso ao Code. Se aparecer um pedido de login ou de plano, resolva esse acesso antes de colar o prompt. Os mentores podem acompanhar essa primeira preparação.

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
      configurar-cerebro/
        SKILL.md
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
| [.claude/skills/](.claude/skills/configurar-cerebro/SKILL.md) | Configurar a base com configurar-cerebro; receber com cerebro; registrar e compartilhar com salvar. |

## 1. Criar a base da empresa

Esta etapa é feita uma vez por empresa. Quem vai usar uma base já criada começa na etapa 2, depois de aceitar o convite de acesso.

1. Cada pessoa cria sua própria conta no [GitHub](https://github.com/signup).
2. Abra o [repositório modelo](https://github.com/jesilveiraa/segundo-cerebro-modelo).
3. Clique em **Use this template > Create a new repository**.
4. Escolha quem será proprietário: uma conta de uma das pessoas ou uma organização da empresa. Escolha o nome da base, como `empresa-os`, e selecione **Private**.
5. Clique em **Create repository from template**. Crie uma única base para a empresa.
6. Se usou uma conta pessoal, abra **Settings > Collaborators > Add people** e convide a outra pessoa. Ela precisa aceitar o convite com a conta dela. Em uma organização, conceda acesso de escrita às pessoas que vão trabalhar na base.
7. Copie o link da base que acabou de criar. Esse é o link que as duas vão usar, não o link deste modelo público.

A cópia da empresa tem vida própria. Mudanças futuras neste modelo não substituem automaticamente seus arquivos.

## 2. Trazer a base para cada computador

Use o **Claude Code em ambiente local**, com acesso aos arquivos e à execução de comandos. Uma conversa comum sem acesso ao computador não consegue fazer esta etapa.

Abra uma pasta local de trabalho no Claude Code. Use o prompt abaixo, preenchendo somente o link da base da empresa e seu nome. A IA ajuda a escolher onde criar a pasta; você não precisa escrever um caminho completo. Se já tiver escolhido um local, informe isso na conversa. No segundo computador, use o mesmo link e o nome da pessoa que está trabalhando.

### Prompt para copiar a base

```text
Quero trazer o cérebro da minha empresa para este computador.

Repositório da empresa: <LINK_DO_REPOSITORIO_PRIVADO_DA_EMPRESA>
Quem está trabalhando: <MEU_NOME>

Confira o acesso local, o Git e o acesso ao GitHub. Se faltar algo,
me guie pelo fluxo oficial, sem pedir senha ou token nesta conversa.
Crie uma pasta com o nome dessa base em um local de trabalho fora de
OneDrive, iCloud e Dropbox. Se o local não estiver claro, me ajude a escolher.
Preserve arquivos existentes; reutilize a pasta se já for essa mesma base.
Copie a base privada indicada, sem criar outro repositório nem alterar
outros projetos. Confira que a ligação é com ela, não com o modelo público.
Leia README.md, AGENTS.md e CLAUDE.md e confira a skill configurar-cerebro.
Ao terminar, diga qual pasta abrir no Claude Code e entregue o próximo
pedido pronto para copiar: /configurar-cerebro, com meu nome e o link acima.
O preenchimento da identidade, o log e o teste de envio ficam para essa skill.
Se ela não aparecer, me oriente a abrir uma nova sessão na pasta criada
ou pedir que leia .claude/skills/configurar-cerebro/SKILL.md e siga a rotina.
```

O Git e a autenticação precisam estar disponíveis em cada computador. Siga as telas oficiais de acesso quando solicitado. As skills orientam a rotina, mas não substituem essas permissões.

## 3. Configurar a base em cada computador

1. Abra a pasta criada no Claude Code.
2. Use `/configurar-cerebro` e informe seu nome e o link da base da empresa, como orientado pelo prompt.
   Você pode copiar o pedido pronto que a IA entregou no fim da etapa 2.
3. Responda ao que faltar sobre a empresa e seu papel. No segundo computador, a skill aproveita a identidade já preenchida pela primeira pessoa.
4. Siga as telas oficiais se houver alguma pendência de acesso. A skill confere que a base é privada e que consegue receber as atualizações.
5. A skill ajusta a apresentação da empresa, registra a sessão no LOG.md e usa salvar para enviar esses ajustes e testar a escrita.
6. Confira o resultado: pasta aberta, base escolhida, recebimento, envio e pendências. Um resultado parcial deve indicar o que falta.

Essa configuração é feita em cada computador. A skill confere a ligação com a base escolhida; as rotinas cerebro e salvar usam essa ligação para sincronizar. O nome da empresa e o link não precisam ser escritos dentro das skills.

Teste a troca com outra pessoa: uma altera um critério real em um arquivo e usa salvar; a outra usa cerebro e mostra a alteração recebida. Depois façam o caminho de volta. A configuração de um computador só comprova o acesso dele.

## 4. Usar no dia a dia

1. Ao começar, use `/cerebro` e diga seu nome e o assunto em que quer trabalhar. Exemplo: `/cerebro vamos registrar como preparamos reuniões`.
2. Trabalhe com a IA e confira os arquivos usados como fonte. Cadastre clientes apenas quando houver contexto real para guardar.
3. Ao terminar, use `/salvar`.
4. Confira quais arquivos foram salvos, se o envio foi confirmado e quais pendências ficaram.

- **configurar-cerebro:** prepara a base neste computador ou retoma uma configuração incompleta.
- **cerebro:** recebe atualizações e lê o contexto relevante para começar.
- **salvar:** atualiza os registros nos lugares certos, acrescenta a sessão ao log e compartilha as alterações.

Salvar no computador não garante que o conteúdo chegou à outra pessoa. Se faltar internet ou acesso, a IA deve dizer o que ficou local. Se as duas alterarem o mesmo conteúdo, a rotina compara as versões e pede ajuda somente quando houver uma decisão de significado em aberto.

As skills também podem ser usadas por um pedido claro, como “configure esta base neste computador”, “atualize o cérebro antes de começarmos” ou “salve e compartilhe o trabalho desta sessão”.

Se precisar de ajuda, copie: “Confira o que falta para receber ou salvar as atualizações. Preserve meus arquivos e explique o próximo passo em linguagem simples.”

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
