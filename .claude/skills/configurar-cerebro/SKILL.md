---
name: configurar-cerebro
description: Configurar o segundo cérebro da empresa no computador depois da cópia inicial, conferindo pasta, acesso ao GitHub, destino de sincronização, identidade, log e recebimento e envio. Usar também para retomar uma configuração incompleta ou preparar o segundo computador.
---

# Configurar cérebro

Prepare uma base já copiada para o computador. O pedido de configurar inclui registrar e compartilhar os ajustes desta sessão na base privada da empresa, depois de conferir o destino. Use as rotinas [cerebro](../cerebro/SKILL.md) e [salvar](../salvar/SKILL.md) para receber e enviar; elas consultam origin e não precisam de um endereço fixo por empresa.

## 1. Conferir a pasta e a base

Leia [README.md](../../../README.md), [AGENTS.md](../../../AGENTS.md), [CLAUDE.md](../../../CLAUDE.md), [identidade.md](../../../identidade.md) e os registros recentes de [LOG.md](../../../LOG.md).

Confira acesso local a arquivos, execução de comandos e Git. Identifique a raiz com `git rev-parse --show-toplevel`; execute os comandos somente nessa base. Confira `git status --short --branch`, `git branch --show-current`, `git remote get-url origin` e operações Git incompletas. Preserve alterações e versões locais anteriores; não misture trabalhos de origem desconhecida.

Se a base ainda não foi copiada, siga o prompt inicial do README antes de retomar. Não inicialize um repositório dentro de outra base nem trate uma pasta agregadora como repositório.

Compare origin com o link da empresa fornecido na conversa ou já confirmado no README. Endereços HTTPS e SSH podem representar o mesmo proprietário e repositório. Não exiba credenciais caso estejam indevidamente incluídas em uma URL. Se só houver origin, apresente o proprietário e o nome da base e peça confirmação de que é a base da empresa. A confirmação existente nesta sessão pode ser reutilizada.

O destino deve ser o repositório próprio da empresa, na branch main. Se for `jesilveiraa/segundo-cerebro-modelo`, outro destino ou outra branch, pare antes de editar ou enviar e explique a pendência. Uma diferença não autoriza mudar origin, renomear pastas ou alterar o histórico de outra base.

Confira que a base é privada. Use o GitHub CLI ou uma ferramenta GitHub disponível, se houver, ou peça que a pessoa confira **Private** na página da base. Com GitHub CLI, `gh repo view <proprietario>/<repositorio> --json nameWithOwner,url,visibility` permite consultar a visibilidade. A autenticação do CLI pode diferir daquela usada pelo Git. Se a consulta falhar, não conclua que o acesso do Git também falhou. Se estiver pública ou a visibilidade não puder ser confirmada, não envie informações da empresa; explique como conferir ou ajustar no GitHub antes de continuar.

## 2. Conferir o acesso deste computador

Identifique a pessoa pela conversa ou confirmação, sem deduzir pelo login, computador ou autoria Git. Pergunte seu nome se faltar. Cada pessoa usa sua própria conta e seu próprio acesso à mesma base.

Confira a autenticação pelo fluxo oficial do GitHub disponível neste computador. Se faltar acesso, oriente as telas de login ou aceite do convite. Não peça senha, token ou arquivo de credenciais na conversa. Não crie contas, repositórios ou convites como parte desta rotina. Não instale ferramentas, altere configurações globais ou troque outras contas silenciosamente; explique a necessidade e siga o caminho escolhido pela pessoa.

Confira a autoria Git efetiva com `git var GIT_AUTHOR_IDENT`. Se nome ou e-mail estiverem ausentes ou a pessoa precisar usar outros nesta base, obtenha os dados dela e use somente `git config --local user.name <nome>` e `git config --local user.email <email>`. Pode usar o e-mail de privacidade fornecido pelo GitHub. Não adivinhe o e-mail nem use esses dados para determinar a autoria do LOG.md.

Execute cerebro para receber as atualizações antes de editar. Leia novamente os documentos se tiverem mudado. Se houver falha de acesso, conflito ou estado divergente que impeça continuar, preserve os arquivos e siga a orientação dessa rotina. Não declare recebimento comprovado sem consulta remota bem-sucedida.

## 3. Personalizar com informações reais

Reutilize a identidade e as fontes já preenchidas. No segundo computador, preserve a identidade compartilhada e os registros da outra pessoa. Pergunte apenas o que faltar: nome da empresa, o que faz e para quem, nome e papel de quem trabalha. Princípios, tom e forma de trabalhar podem continuar como `a definir` até serem discutidos.

Atualize identidade.md somente com respostas ou fontes confirmadas. Indique data, origem e o que ainda falta validar. Não cadastre clientes fictícios nem trate a configuração como validação de processos.

No README da base da empresa:

- Substitua a apresentação de modelo público por uma apresentação da empresa, usando seu nome confirmado. Se ainda faltar, mantenha uma apresentação genérica de base da empresa.
- Acrescente ou atualize uma seção **Base da empresa**, com o link confirmado do repositório próprio, a visibilidade conferida, data e fonte. Não registre senhas, tokens ou caminhos pessoais dos computadores.
- Ajuste o nome da pasta na árvore para o nome real da pasta local. Os nomes locais podem variar entre computadores; preserve o nome já documentado se a diferença for apenas local.
- Preserve o guia, o prompt inicial, os links de origem do modelo e as fontes e conexões já existentes. Diferencie os links de referência ao modelo do destino de sincronização da empresa.

Não reescreva as skills cerebro e salvar para fixar nome, caminho ou link da empresa. O clone já cria a pasta de destino e configura origin; a configuração verifica esse resultado. Não renomeie o modelo público nem crie uma segunda base para a mesma empresa.

## 4. Registrar e testar a sincronização

Registre a sessão em LOG.md com data real, autoria humana, Claude Code como apoio, ajustes e documentos, fonte e pendências. Descreva separadamente o acesso recebido e o envio ainda a conferir. Preserve as entradas existentes. Se esta sessão já estiver registrada e não houver trabalho novo, retome a conferência sem duplicá-la.

Execute salvar para revisar e enviar somente os ajustes desta sessão. O registro real da configuração é suficiente para testar a escrita; não crie arquivos de teste, versões vazias ou alterações artificiais. Se houver apenas pendências de um envio anterior, retome esse envio conforme salvar. Se não houver nada novo a enviar nem envio anterior pendente, informe que esta execução não testou uma nova escrita.

Confirme o envio pela conferência remota prevista em salvar. Se falhar, informe o que ficou local. Não escreva no log que o envio foi confirmado antes dessa conferência nem crie um ciclo de novas versões apenas para registrar cada envio.

O teste deste computador não comprova a troca entre duas pessoas. Oriente a demonstração prevista no README: uma salva uma alteração real; a outra recebe com cerebro e mostra o conteúdo; depois fazem o caminho de volta. Registre essa troca como pendente até existir evidência.

## 5. Entregar o resultado

Informe a pasta que deve ficar aberta, o nome e link da base compartilhada, os documentos ajustados e os resultados separados: leitura recebida, escrita enviada e troca entre computadores. Cite as pendências reais de acesso ou identidade.

Mostre a rotina: `/cerebro` ao começar e `/salvar` ao terminar. Configurar-cerebro é usado na preparação ou quando houver necessidade de retomar ajustes, não em toda sessão.

Se a skill não aparecer no Claude Code, oriente abrir uma nova sessão na pasta clonada. Como alternativa, leia este SKILL.md e siga a rotina diretamente. Esta configuração não instala agendadores, conecta ferramentas externas, publica materiais ou compartilha acessos.
