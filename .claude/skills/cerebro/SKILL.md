---
name: cerebro
description: Receber as atualizações da base da empresa e ler o contexto relevante ao começar uma sessão ou quando a pessoa pedir para atualizar o cérebro.
---

# Cerebro

Atualize a cópia local da base e prepare o contexto solicitado. Responda em português simples. Execute as operações de recebimento pelo acesso local disponível; não entregue uma lista de comandos para a pessoa executar quando você puder fazer o trabalho.

## Conferir o ambiente

- Localize a raiz real da base com `git rev-parse --show-toplevel`. Faça os comandos nessa pasta, não em uma pasta agregadora ou em outro repositório.
- Leia AGENTS.md e o mapa do README. Confirme a branch, o destino de sincronização e o estado com `git branch --show-current`, `git remote get-url origin` e `git status --short --branch`. Não exponha credenciais presentes em configurações.
- A rotina da empresa usa main e origin apontando para a base própria. Se estiver no modelo público `jesilveiraa/segundo-cerebro-modelo`, em outra branch, sem origin, ou com uma operação Git incompleta, explique o que falta antes de mudar qualquer estado. Não trocar branch ou destino automaticamente.
- Se não houver Git, autenticação, rede ou execução local, preserve os arquivos e informe a limitação. Oriente a configuração necessária sem pedir senhas ou tokens na conversa.

## Receber sem perder trabalho

1. Consulte as atualizações com `git fetch origin`. Se falhar, não chame a base de atualizada. Pode ler a cópia local, identificando que a atualização não foi confirmada.
2. Compare `HEAD` com `origin/main` usando `git rev-list --left-right --count HEAD...origin/main`. O primeiro número representa versões só locais; o segundo, versões ainda a receber.
3. Se não houver versões a receber, preserve tudo. Alterações locais e versões ainda não enviadas são pendências de salvar, não razão para apagá-las.
4. Se houver apenas versões a receber, use `git merge --ff-only origin/main`. Isso só avança o histórico. O Git pode preservar mudanças locais compatíveis; se recusar por sobreposição, pare a atualização e mostre os arquivos envolvidos. Não guardar mudanças com stash, fazer commit ou enviar trabalho como efeito de cerebro. Informe como continuar pela rotina salvar, conforme o pedido da pessoa.
5. Se os dois lados tiverem versões diferentes, preserve o estado e compare os trabalhos com `git log --oneline HEAD...origin/main` e as diferenças dos arquivos relevantes. Oriente a combinação pela rotina salvar. Não reescrever o histórico ou iniciar uma resolução sem compreender o conteúdo.
6. Confira novamente o estado. Diga se recebeu as atualizações, se já estava em dia ou se a cópia local continua com recebimento pendente. Não confundir versões locais não enviadas com sincronização concluída.

## Ler o contexto e começar

Depois de receber, ou de identificar a limitação:

- Leia identidade.md, os registros recentes de LOG.md e a entrada de processos ou clientes indicada pelo assunto. Siga os links relevantes, sem carregar todo o acervo.
- Identifique quem conduz a sessão pela conferência de autoria abaixo. Não pedir o nome de novo se o cadastro já estiver confirmado para esta cópia.
- Se a pessoa não indicou o assunto, apresente o mapa e peça apenas a prioridade necessária para continuar. Não invente uma tarefa ou uma fila de prioridades.
- Uma versão atual da pasta não comprova dados atuais de ferramentas externas. Consulte essas fontes pelos conectores somente quando a tarefa exigir e houver acesso autorizado.

## Reconhecer a pessoa

1. Se a pessoa se identificou explicitamente nesta sessão, use esse nome. Se for diferente do cadastro local, essa identificação vale para a sessão; não substitua o cadastro permanente sem confirmar.
2. Caso contrário, leia a seção Pessoa desta cópia em CLAUDE.local.md. Confira nome, conta GitHub, fonte da confirmação e se o proprietário/repositório corresponde ao origin atual, considerando HTTPS e SSH equivalentes.
3. Quando houver acesso ao GitHub CLI, consulte `gh api user --jq .login`; outra ferramenta GitHub autenticada também pode identificar a conta. Se corresponder ao cadastro, use o nome confirmado, sem nova pergunta. Se a conta for diferente, confirme quem está trabalhando antes de atribuir o log. Não tratar a conta nova como a pessoa anterior.
4. Se a consulta à conta estiver indisponível, pode usar o cadastro local já confirmado e pertinente à base, enquanto não houver evidência de troca de pessoa ou conta. Indique a limitação de autenticação quando afetar a tarefa. Ausência de internet não apaga a identidade cadastrada.
5. Sem cadastro confirmado, com base diferente ou em situação ambígua, pergunte uma vez quem trabalha e mantenha a autoria como a confirmar até receber a resposta. Oriente configurar-cerebro para guardar a associação local. Não deduzir o nome humano pelo login, nome do computador ou autoria Git, nem adotar o cadastro recebido de outra pessoa.

## Resposta

Informe o estado do recebimento, mudanças relevantes, arquivos consultados e pendências. Comece a tarefa já pedida quando houver contexto suficiente. Exemplo de resultado: “Recebi as atualizações. Li a identidade e o processo de reuniões. Há uma alteração local ainda a compartilhar.”

Receber arquivos não concede acesso a outros sistemas e não autoriza mensagens, publicação ou criação de repositórios.
