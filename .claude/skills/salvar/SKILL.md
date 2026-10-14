---
name: salvar
description: Registrar e revisar o trabalho da sessão e concluir o salvamento na main da base privada quando a pessoa pedir para salvar, compartilhar ou encerrar. Usar também ao concluir configurar-cerebro.
---

# Salvar na base compartilhada

O resultado é o trabalho revisado, registrado e confirmado em main no GitHub. A pessoa não precisa gerenciar branches ou executar comandos. O pedido de salvar, compartilhar, encerrar ou configurar-cerebro autoriza enviar as alterações desta sessão à base privada conferida, sem autorizar mudanças em outros sistemas.

## Conferir base e autoria

Leia README.md, AGENTS.md e CLAUDE.md. Identifique a raiz, origin, branch atual, estado e operações Git incompletas. Compare origin com a base da empresa confirmada na conversa ou no README. HTTPS e SSH podem representar o mesmo repositório. Não expor credenciais.

Não enviar para o modelo público jesilveiraa/segundo-cerebro-modelo, base desconhecida ou destino diferente do confirmado. Na manutenção explícita do modelo, seguir a exceção de AGENTS.md; ela nunca autoriza publicar dados de uma empresa. Não trocar origin para resolver a diferença.

O Cloud pode usar uma branch de sessão. Não exigir checkout de main, nem rejeitar a tarefa só pelo nome da branch. Inspecionar alterações não registradas, conteúdo preparado e commits da branch que ainda não estão em origin/main. A autorização cobre somente o trabalho desta sessão e retomadas explicitamente identificadas. Preservar conteúdo alheio e não incluir commits anteriores de origem desconhecida.

Reutilizar quem se identificou na conversa. Se faltar confirmação ou houver ambiguidade, perguntar uma vez antes de atribuir o log. Autoria Git é dado técnico, não prova do nome humano. Se faltar configuração necessária para commit, pedir os dados e configurar somente nesta base; não inventar e-mail.

## Organizar e revisar

1. Guardar cada informação na sua fonte: identidade em identidade.md, procedimentos em processos, resultados e particularidades no cliente. Atualizar índices quando criar documentos.
2. Distinguir fatos, decisões, propostas e pendências, com data e fonte. Preservar fontes históricas e não inventar clientes, acessos ou compromissos.
3. Acrescentar o registro da sessão em LOG.md com autoria, apoio de IA, trabalho e links, resultado, pendências e fonte. Se houver apenas retomada de um envio já registrado, não duplicar a entrada. Não afirmar envio antes de conferir.
4. Conferir diferenças, arquivos novos e conteúdo preparado, incluindo `git diff --check`. Não incluir credenciais, arquivos pessoais ignorados ou conteúdo fora do escopo. Se houver conteúdo preparado alheio, preservá-lo e separar o escopo antes de commit.

## Concluir em main

Execute pelo Git disponível nesta base. Não fixar o nome da branch da sessão no procedimento.

1. Receber `origin` com `git fetch origin`. Confirmar que origin/main existe. Se faltar acesso, referência ou houver operação incompleta, preservar e informar a pendência; não inventar um destino.
2. Preparar e registrar somente caminhos ou trechos revisados desta sessão. Usar commit quando houver conteúdo novo preparado; não criar commit vazio para comprovar envio. Se uma tentativa anterior já registrou o trabalho, retomar desse estado.
3. Comparar HEAD com origin/main e revisar diferenças e commits envolvidos. Se HEAD já contiver origin/main, manter. Se estiver somente atrás, avançar sem reescrever histórico. Se houver versões de ambos os lados, combinar origin/main na branch atual com merge, preservando os dois trabalhos. Não usar rebase, reset, stash, limpeza ou força para descartar ou ocultar alterações.
4. Em conflito, ler a base e os dois lados. Preservar entradas independentes do log e conteúdo compatível. Só concluir a combinação quando o significado estiver claro; uma decisão sem evidência exige confirmação. Não escolher um lado inteiro automaticamente nem declarar salvamento com conflito pendente.
5. Conferir que o histórico pronto para envio contém a main recebida e somente alterações conhecidas e autorizadas além dela. Enviar a versão da sessão com `git push origin HEAD:main`. Não usar `git push origin main` quando a branch local main estiver desatualizada: esse comando pode enviar outra versão, em vez do trabalho da sessão.
6. Se outra pessoa avançou main e o envio for recusado por concorrência, receber e combinar novamente, rever o resultado e tentar uma vez. Uma nova recusa, falha de acesso ou proteção de main encerra a tentativa. Não alterar regras, permissões ou forçar o envio. Se a base exigir PR, preservar e explicar o que falta para concluir a integração; PR aberto sozinho não é main atualizada.
7. Após o envio, conferir main remota. Comparar a versão enviada com `git ls-remote origin refs/heads/main`. Se main avançou novamente, fazer fetch e conferir `git merge-base --is-ancestor <versao-enviada> origin/main`: sucesso comprova inclusão do trabalho. Se a consulta falhar ou não comprovar inclusão, informar confirmação pendente.
8. Conferir o estado restante. Se houver mudanças ou commits fora do que foi enviado, informar o que permanece pendente; não chamar toda a sessão de salva.

## Resposta

Dizer o que foi registrado, onde está e se main contém o trabalho. Exemplo, somente com comprovação: “Salvei o processo e o log na base compartilhada. A outra pessoa já pode consultar a versão atualizada.”

Se não concluiu: “Os arquivos estão preservados na sessão. Ainda falta concluir o salvamento na base compartilhada por [motivo e próximo passo].” Não chamar uma branch enviada ou PR aberto de salvamento concluído.

Esta rotina não cria repositórios ou convites, publica materiais para clientes, envia mensagens, conecta ferramentas ou instala agendadores.
