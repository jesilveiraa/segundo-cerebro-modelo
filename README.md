# Segundo cérebro da empresa

Uma base em arquivos para guardar contexto, processos e conhecimento do trabalho. O Claude Code consulta e atualiza esses arquivos; o GitHub guarda as versões compartilhadas.

Este é um **modelo público da LÍNIA Consultoria**. O prompt inicial orienta o Claude a criar uma base privada própria antes de trabalhar. As pessoas da mesma empresa usam essa mesma base, cada uma com sua conta e sua pasta no computador.

## Por onde começar

| Sua situação | Comece aqui |
|---|---|
| A empresa ainda não tem uma base | Use o primeiro prompt. O Claude cria a base, convida a outra pessoa e prepara sua pasta. |
| Outra pessoa já criou a base da empresa | Aceite o convite e use o segundo prompt com o link recebido. |
| A base já está configurada neste computador | Use cerebro, trabalhe e use salvar. |

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

## 1. Preparar os acessos

Cada pessoa cria sua própria conta no [GitHub](https://github.com/signup). Abra o Claude no modo Code em ambiente local. O Claude orienta o acesso ao GitHub quando necessário; entrar na conta e responder às telas de autorização ainda depende da pessoa.

A empresa usa uma única base. Uma pessoa inicia a criação; a outra aceita o convite e utiliza essa mesma base. A primeira informa o **usuário GitHub** da outra, que aparece no perfil dela. Não é necessário compartilhar senhas.

## 2. Primeira pessoa: criar e preparar a base

Preencha os dois campos abaixo. O nome será usado na base do GitHub e na pasta local, por exemplo `empresa-os`.

### Prompt para criar a base

```text
Quero preparar o segundo cérebro da minha empresa neste computador.

Nome da base: <NOME_DA_EMPRESA-os>
Usuário GitHub da pessoa que vai trabalhar comigo: <USUARIO_GITHUB>

Confira o acesso local, o Git e o GitHub. Se faltar algo, me guie pelo
fluxo oficial de instalação e login, sem pedir senha ou token nesta conversa.
Confira a conta GitHub autenticada e use essa conta como proprietária.
Crie uma base PRIVADA a partir deste modelo:
https://github.com/jesilveiraa/segundo-cerebro-modelo
Se já existir uma base com esse nome, confira comigo antes de reutilizar.
Confira o perfil do usuário indicado e convide somente essa pessoa,
com permissão de escrita. Preserve permissões existentes e não duplique convites.
Confira o resultado e me diga se o convite está pendente de aceite.
Espere os arquivos do modelo ficarem disponíveis antes de copiar a base.
Copie a base para uma pasta local fora de OneDrive, iCloud e Dropbox.
Preserve arquivos existentes e não altere outros projetos ou acessos.
Leia o README e as instruções da pasta criada. Leia e siga
.claude/skills/configurar-cerebro/SKILL.md para concluir a preparação.
Confirme uma vez meu nome para o log e vincule-o à minha conta GitHub,
em um cadastro local que não seja enviado para a outra pessoa.
Ao terminar, diga qual pasta abrir no Claude Code e entregue o link
que a outra pessoa deve usar. Informe o que foi conferido e o que falta.
```

O prompt autoriza criar essa base privada e enviar esse convite. O convite precisa ser aceito pela pessoa convidada. A IA deve conferir privacidade, destino e resultado antes de afirmar que os acessos estão prontos.

Se for necessário abrir uma nova sessão na pasta criada, a IA entrega `/configurar-cerebro` pronto para copiar e retoma o que já foi feito. Você não precisa reconstruir os dados da configuração.

## 3. Segunda pessoa: usar a base já criada

Aceite o convite com sua conta GitHub. Depois abra o Claude Code local e cole o prompt abaixo, preenchendo somente o link que a primeira pessoa recebeu.

### Prompt para copiar a base

```text
Quero usar o segundo cérebro da minha empresa neste computador.

Repositório da empresa: <LINK_DA_BASE_PRIVADA_DA_EMPRESA>

Confira o acesso local, o Git e o GitHub. Se faltar algo, me guie pelo
fluxo oficial de instalação e login, sem pedir senha ou token nesta conversa.
Use minha própria conta GitHub e confira o acesso à base indicada.
Se o convite ainda não foi aceito, me oriente a aceitá-lo.
Copie essa mesma base para uma pasta local fora de OneDrive, iCloud e Dropbox.
Preserve arquivos existentes; reutilize a pasta se já for essa base.
Não crie outro repositório nem envie novos convites.
Leia o README e as instruções da pasta criada. Leia e siga
.claude/skills/configurar-cerebro/SKILL.md para concluir a preparação.
Confirme uma vez meu nome para o log e vincule-o à minha conta GitHub,
em um cadastro local que não seja enviado para a outra pessoa.
Aproveite a identidade e os registros já preenchidos, sem substituí-los.
Ao terminar, diga qual pasta abrir no Claude Code, o que foi conferido
sobre recebimento e envio e qualquer pendência.
```

Configurar-cerebro confere a base privada, prepara o cadastro da pessoa neste computador, pergunta o que faltar sobre a empresa, ajusta os documentos e registra a sessão no LOG.md. Usa cerebro e salvar para conferir recebimento e envio. A criação da base e o convite ficam no primeiro prompt; a skill trabalha na base já copiada.

O cadastro da pessoa fica em `CLAUDE.local.md`, que acompanha somente esta pasta no computador e é ignorado pelo Git. Não guarda senhas. Cada pessoa configura seu próprio cadastro. A identidade da empresa e o log do trabalho ficam na base compartilhada.

Uma base gerada tem vida própria. Melhorias futuras no modelo não substituem automaticamente os arquivos da empresa.

## 4. Conferir a troca entre as duas

Uma pessoa registra uma informação real e usa salvar. A outra usa cerebro e mostra a informação recebida. Depois fazem o caminho de volta. A configuração de uma pasta só comprova o acesso daquele computador.

## 5. Usar no dia a dia

1. Abra a pasta da empresa no Claude Code.
2. Ao começar, use `/cerebro` e diga o assunto. Exemplo: `/cerebro vamos registrar como preparamos reuniões`.
3. Trabalhe com a IA e confira os arquivos usados como fonte.
4. Ao terminar, use `/salvar` e confira se o envio foi confirmado.

Depois da configuração, não precisa dizer seu nome em cada sessão. A IA usa o cadastro confirmado desta cópia e confere a conta GitHub disponível. Se a conta mudar, faltar o cadastro ou outra pessoa estiver usando o computador, confirma a autoria antes de registrar o trabalho.

- **configurar-cerebro:** prepara a base neste computador ou retoma uma configuração incompleta.
- **cerebro:** recebe atualizações, reconhece a pessoa cadastrada e lê o contexto relevante.
- **salvar:** atualiza os documentos e o log e compartilha o trabalho.

Salvar no computador não garante que o conteúdo chegou à outra pessoa. Se faltar internet ou acesso, a IA informa o que ficou local. Se houver mudanças incompatíveis, compara os conteúdos e pede ajuda quando existir uma decisão de significado em aberto.

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

Referências: [criação pelo GitHub CLI](https://cli.github.com/manual/gh_repo_create), [convite de colaboração](https://docs.github.com/en/rest/collaborators/collaborators#add-a-repository-collaborator), [autenticação](https://cli.github.com/manual/gh_auth_login), [instruções locais do Claude](https://code.claude.com/docs/en/memory), [modelo no GitHub](https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-repository-from-a-template), [cópia local](https://docs.github.com/en/repositories/creating-and-managing-repositories/cloning-a-repository), [Claude Code local](https://code.claude.com/docs/en/desktop), [skills do Claude Code](https://code.claude.com/docs/en/skills) e [Conectores](https://support.claude.com/en/articles/11176164-use-connectors-to-extend-claude-s-capabilities).
