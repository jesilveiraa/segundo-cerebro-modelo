# Como trabalhar nesta base

@AGENTS.md

## Ao iniciar ou retomar um trabalho

A pessoa começa dizendo o que precisa fazer. Não exigir uma skill de início. O conhecimento continua em identidade, processos e clientes; este arquivo orienta a leitura e a atualização.

1. Identificar a raiz com `git rev-parse --show-toplevel` e operar somente nela. Conferir `git status --short --branch`, a branch atual, origin e operações incompletas. Origin precisa corresponder à base da empresa confirmada na conversa ou no README. Não expor credenciais de URLs.
2. O Cloud pode estar na branch criada para a sessão. Isso não é erro de configuração: main é a versão compartilhada e o destino final, não uma exigência sobre a branch de trabalho. Não trocar branch ou origin automaticamente.
3. Conferir a versão compartilhada com `git fetch origin`. Quando necessário, combinar `origin/main` com a branch atual, sem descartar arquivos ou versões. Usar avanço direto quando possível; diante de históricos divergentes, ler as diferenças antes de combinar. Não criar commit ou enviar como efeito da leitura inicial. Se a combinação exigir commit, encaminhar a conclusão por salvar, dentro do escopo autorizado. Se mudanças não registradas impedirem receber, preservá-las e explicar como concluir o salvamento antes de retomar. Não usar stash, reset, limpeza ou envio forçado para contornar.
4. Se fetch falhar, informar que a atualização não foi confirmada. Não tratar uma sessão antiga como atualizada só por estar aberta. Se o histórico impedir continuar, preservar o trabalho e explicar a pendência.
5. Ler README.md, contexto-da-empresa/identidade.md, registros recentes de LOG.md e os arquivos das áreas pertinentes em contexto-da-empresa/, processos/mapa-dos-processos.md ou clientes/. Consultar as fontes necessárias ao pedido, sem ler todo o acervo por padrão. Se a atualização mudar documentos já lidos, consultar a versão recebida.
6. Reutilizar a identificação explícita da pessoa nesta sessão. Se faltar evidência ou houver ambiguidade, perguntar uma vez quem conduz e manter a autoria a confirmar até a resposta. Não deduzir nome humano pelo login ou pela autoria Git. Não depender de CLAUDE.local.md nem criar cadastro permanente no computador.
7. Começar a tarefa quando houver contexto suficiente. Só perguntar prioridade se o pedido não indicar o que fazer. Dados atuais de serviços externos precisam de consulta própria, não são comprovados por atualizar o repositório.

Na preparação inicial ou retomada de uma preparação incompleta, seguir configurar-cerebro. Na rotina, a pessoa pode pedir o trabalho diretamente. Ao pedir salvar, compartilhar ou encerrar, seguir salvar.

## Resultado do salvamento

O resultado esperado é o trabalho registrado, revisado e confirmado em main no GitHub. A skill salvar recebe as atualizações, combina os trabalhos e envia a versão da sessão para main. Não deixar uma branch ou PR como se fossem salvamento concluído.

Se acesso, proteção da base ou conflito impedir concluir, preservar os arquivos e informar a pendência. Não contornar proteções ou forçar envio. A pessoa não precisa executar comandos Git nem gerenciar branches; explicar os resultados em linguagem simples.
