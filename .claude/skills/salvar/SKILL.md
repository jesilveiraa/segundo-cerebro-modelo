---
name: salvar
description: Registrar o trabalho da sessão nos arquivos da empresa, acrescentar o log e enviar as alterações à base compartilhada quando a pessoa pedir para salvar, compartilhar ou encerrar o trabalho.
---

# Salvar

Transforme o trabalho da sessão em registros úteis e compartilhe as alterações pela base configurada. Um pedido claro de salvar, compartilhar ou encerrar autoriza esse envio. O pedido de configurar-cerebro também inclui enviar os ajustes dessa configuração para a base privada já conferida. Se não houve um desses pedidos, registre o que já foi autorizado localmente e não envie por iniciativa própria.

## Conferir a base e o escopo

Leia AGENTS.md e README.md. Identifique a raiz real com `git rev-parse --show-toplevel` e execute os comandos nela. Confira `git status --short --branch`, `git branch --show-current`, `git remote get-url origin` e eventuais operações incompletas. Não exiba credenciais de configurações.

A base usa main e origin apontando para o repositório próprio da empresa. Não enviar para o modelo público `jesilveiraa/segundo-cerebro-modelo`, outro repositório ou outra branch. Se o destino ou estado não estiver correto, preserve o trabalho e explique a pendência. Não mudar destinos, configurar Git globalmente ou instalar agendadores.

Identifique o conteúdo desta sessão e o que já existia. Revise as diferenças e eventuais versões locais ainda não enviadas. Não incluir alterações ou versões anteriores de origem desconhecida sem esclarecer o escopo. Mudanças alheias continuam preservadas.

## Atualizar os registros

1. Reutilize a pessoa reconhecida nesta sessão pela conferência de autoria de cerebro, ou a identificação explícita na conversa. Se a autoria ainda não tiver sido conferida, siga somente essa conferência, sem executar de novo toda a atualização. O cadastro local confirmado evita perguntar o nome a cada envio; peça confirmação quando faltar evidência ou a conta mudar. Cite a ferramenta de IA como apoio.
2. Separe fatos, decisões confirmadas, propostas e pendências. Não converter uma ideia em procedimento validado nem inventar data, responsável ou acesso.
3. Salve cada informação em sua fonte: identidade da empresa em identidade.md; critérios e procedimentos em processos/; contexto e resultado específico em clientes/<cliente>/. Fontes e conexões gerais ficam no README da raiz; as específicas, no cliente.
4. Quando criar arquivos, atualize os índices relevantes. Crie cliente somente quando houver contexto real. Preserve fontes históricas e acrescente data e origem das correções.
5. Acrescente a sessão em LOG.md, com data real, autoria, apoio de IA, trabalho e links, resultado e pendências e fonte. O registro descreve o trabalho; não afirma que o envio aconteceu antes da conferência. Não copiar conversas inteiras, credenciais ou controles de tarefas. Se esta sessão já estiver registrada e não houver trabalho novo, apenas retome o envio, sem duplicar a entrada.

## Registrar e compartilhar

Use o Git disponível, preservando os dados e o histórico:

1. Consulte `git diff`, `git diff --cached`, `git ls-files --others --exclude-standard` e `git diff --check`. Confira também arquivos novos. Não enviar credenciais, conteúdo fora da sessão ou arquivos locais ignorados. CLAUDE.local.md é o cadastro pessoal desta cópia e nunca deve ser enviado, mesmo se estiver indevidamente preparado. A existência de .gitignore não substitui a revisão.
2. Se houver alterações já preparadas para envio fora do escopo, preserve-as e esclareça como separar o trabalho antes de registrar. Não misturar nem desfazer a preparação de outra pessoa. Para arquivos com trechos de outra sessão, separar os trechos ou esclarecer o escopo antes de incluí-los.
3. Confira nome e e-mail de autoria Git configurados. Se faltarem, oriente a configuração local da base com dados fornecidos pela pessoa. Essa autoria técnica não determina quem consta no LOG.md.
4. Prepare apenas os caminhos ou trechos desta sessão. Para arquivos inteiros conferidos, use `git add -- <caminhos>` e revise `git diff --cached`. Não usar inclusão indiscriminada de toda a pasta. Registre com `git commit -m <resumo-do-trabalho>` se houver conteúdo preparado. Se uma tentativa anterior já registrou o trabalho, não criar uma versão vazia.
5. Receba a situação remota com `git fetch origin` e compare `HEAD...origin/main`. Se falhar, preserve a versão local e informe que ela ainda não foi compartilhada.
6. Se houver versões só remotas, avance com `git merge --ff-only origin/main`. Se houver versões dos dois lados, confira os conteúdos e combine com `git merge --no-edit origin/main`, somente quando as alterações locais não registradas estiverem preservadas e compatíveis com a operação. Nunca usar envio forçado, reset, limpeza, stash ou rebase para descartar ou ocultar trabalho.
7. Se a combinação tiver conflitos, leia a base e os dois lados dos arquivos. Preserve todas as entradas independentes do log e os conteúdos compatíveis. Conflitos de significado precisam de confirmação da pessoa; mantenha os dois trabalhos disponíveis enquanto pergunta. Não escolher um lado inteiro para resolver. Adicione somente os arquivos cuja resolução foi conferida e conclua a combinação. Não declarar envio concluído com conflitos pendentes.
8. Envie com `git push origin main`. Se outra pessoa tiver enviado nesse intervalo e o Git recusar, repita uma vez a consulta e a combinação, conferindo o conteúdo. Uma nova recusa encerra a tentativa: preserve os arquivos e explique a pendência. Falhas de acesso ou rede não exigem insistência.
9. Consulte a referência remota com `git ls-remote origin refs/heads/main` e compare com `git rev-parse HEAD`. Se for a mesma versão, o envio está confirmado. Se alguém tiver avançado a base depois do envio, receba a referência e confira `git merge-base --is-ancestor HEAD origin/main`: sucesso comprova que sua versão está incluída. Se a conferência falhar, diga que o envio ainda não foi confirmado.
10. Confira `git status --short --branch` e informe mudanças locais remanescentes. Não declarar a pasta inteira sincronizada se houver trabalho que não foi enviado.

## Resposta

Informe quais documentos e log foram atualizados, o resultado da conferência de envio e as pendências. Use linguagem simples: “Salvei os registros e confirmei o envio. A outra pessoa pode recebê-los com cerebro.” Se não conseguiu enviar: “Os arquivos estão preservados neste computador; o compartilhamento ficou pendente por...”

Esta rotina não publica material para clientes, altera sistemas externos, cria repositórios nem compartilha acessos. Essas ações dependem de pedidos próprios.
