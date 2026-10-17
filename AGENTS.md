# Instruções do cérebro da empresa

Esta base pertence à empresa identificada em contexto-da-empresa/identidade.md. O README é seu mapa. Não depender de repositórios, ferramentas ou contas dos mentores.

## Começar

O fluxo de início e atualização fica em CLAUDE.md. O Claude Code o carrega como instrução; outra ferramenta de IA deve lê-lo antes de trabalhar. Consultar contexto e confirmar autoria conforme esse fluxo, sem exigir uma skill de início ou cadastro pessoal local.

Usar fontes reais e indicar data. Distinguir fato confirmado, proposta, hipótese e pendência. Preparação inicial usa configurar-cerebro; salvamento usa salvar.

## Onde guardar

- Identidade e posicionamento: contexto-da-empresa/identidade.md.
- Produtos, serviços e entregas: contexto-da-empresa/produtos-servicos-e-entregas.md.
- Perfis gerais de clientes e mercado: contexto-da-empresa/clientes-e-mercado.md.
- Pessoas e responsabilidades: contexto-da-empresa/pessoas.md.
- Comunicação e referências: contexto-da-empresa/comunicacao-e-referencias.md.
- Jornada do cliente, back office e rotinas: processos/mapa-dos-processos.md. Detalhes de cada processo entram em documentos próprios somente quando houver conteúdo.
- Contexto e resultados específicos: clientes/<cliente>/, com entrada no README do cliente e link em clientes/README.md.
- Fontes e conexões gerais: seção correspondente no README da raiz. Fontes específicas: README do cliente.
- Trabalho realizado em cada sessão: LOG.md.
- Rotinas da IA: .claude/skills/. Consultam os documentos de negócio sem copiar os critérios para dentro da skill.

Criar clientes e documentos somente com material real. Começar com arquivos simples; novas subpastas dependem do conteúdo. Preservar fontes de reunião e seus avisos. Separar transcrição de análise e combinados quando necessários.

## Organização e atualização pela IA

Estas regras são responsabilidade da IA. As pessoas fornecem materiais, esclarecem lacunas e conferem o entendimento; não precisam organizar os arquivos ou preencher metadados manualmente.

- Começar analisando os materiais prontos pertinentes e o contexto já registrado. Mostrar o entendimento e perguntar apenas o que falta. Se não houver material, começar pelo relato. Preencher as áreas gradualmente, sem exigir todas na configuração inicial.
- Manter uma referência principal para cada informação vigente. Antes de registrar, consultar o arquivo adequado e atualizá-lo; usar links onde outro documento precisar do mesmo conteúdo. Não criar cópias concorrentes, um arquivo por conversa ou controles paralelos de agenda, tarefas e indicadores.
- Manter apenas pastas com conteúdo. Os arquivos de contexto do modelo são pontos de partida para preenchimento gradual, não uma exigência de completude. Criar arquivos e subpastas adicionais somente com conteúdo real e necessidade clara. Preservar documentos existentes e comparar seu conteúdo antes de reorganizar.
- Registrar a fonte efetivamente consultada e sua data, quando disponível, além da data do registro ou da revisão. Distinguir essas datas. Não inferir data de origem, vigência, atualidade ou confirmação pela data da sessão. Se faltar, indicar a lacuna e perguntar quando ela mudar o resultado.
- Separar fato confirmado, interpretação, sugestão e pendência. Diante de divergência, apresentar as versões e suas fontes às pessoas para confirmação, sem escolher silenciosamente uma delas.
- Atualizar o conhecimento vigente após confirmação, registrando origem e data da correção. Preservar transcrições e registros históricos; uma correção posterior não reescreve o que foi dito originalmente. O LOG aponta o trabalho feito, sem duplicar o conhecimento.

## Escrever e revisar

Usar português claro, conciso e aplicável. Não usar travessão. Seguir o tom preenchido em contexto-da-empresa/comunicacao-e-referencias.md. Construir e revisar com as pessoas: rascunho não é procedimento validado. Correções indicam fonte e data, preservando registros históricos.

Tarefas atuais, agenda, planilhas e gravações ficam nos sistemas escolhidos. Linkar essas fontes sem criar controles paralelos ou inventar acessos e responsáveis.

## Encerrar

Toda sessão, inclusive análise, recebe entrada em LOG.md: data, quem trabalhou, apoio de IA, trabalho e links, resultado, pendências e fonte. Reaproveitar autoria confirmada na conversa. O log não substitui decisões ou tarefas; preservar entradas anteriores.

O pedido de salvar, compartilhar ou encerrar autoriza registrar e enviar o trabalho da sessão para main na base privada conferida. Configurar-cerebro também inclui esse envio para concluir a preparação. Sem esses pedidos, registrar o que já foi autorizado e informar que o envio está pendente. Não confundir envio para uma branch de trabalho com conclusão em main.

## Sincronização e acesso

A base compartilhada usa main. A sessão pode trabalhar em outra branch, mas deve conferir a situação remota antes de editar e ao salvar. Preservar alterações concorrentes. Só declarar salvamento concluído após conferir que main remota contém o trabalho.

Não enviar informações da empresa para o modelo público jesilveiraa/segundo-cerebro-modelo ou outro destino. A manutenção deste modelo público é uma atividade distinta, permitida somente por pedido explícito de quem o mantém, com arquivos genéricos e sem dados de empresa ou cliente. Registrar essa manutenção separadamente das sessões da empresa no LOG.md.

Não apagar mudanças, usar envio forçado, esconder trabalho com stash ou escolher uma versão de conflito sem comparar os conteúdos. Não trocar destinos, alterar Git globalmente, contornar proteção de branch ou instalar agendadores como parte dessas rotinas.

Não guardar senhas, tokens, credenciais ou bases operacionais neste cérebro. Autenticações usam os fluxos oficiais. Arquivos pessoais ignorados, incluindo CLAUDE.local.md antigo, não devem ser enviados; não usá-los como requisito de autoria. Não compartilhar acessos, enviar mensagens ou publicar materiais para clientes sem pedido próprio.
