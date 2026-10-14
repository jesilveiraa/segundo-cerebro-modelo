---
name: configurar-cerebro
description: Preparar ou retomar a base privada da empresa no Claude Code em Cloud, conferindo repositório, acesso, identidade, mapas e log e concluindo os ajustes em main.
---

# Preparar a base da empresa

A base privada já precisa existir e estar selecionada no Claude Code em Cloud. O pedido de configuração autoriza registrar e salvar os ajustes desta sessão em main, seguindo [salvar](../salvar/SKILL.md). Não exige clone no computador, cadastro pessoal persistente ou skill de início.

## Conferir ambiente e acesso

Leia README.md, AGENTS.md, CLAUDE.md, identidade.md e os registros pertinentes de LOG.md. Siga o início de CLAUDE.md para conferir a base, receber main e identificar a pessoa. Reutilize nome, link e respostas já fornecidos.

Origin deve corresponder à base própria da empresa confirmada. A branch de sessão Cloud é permitida; main é o destino final. Não renomear a branch nem trocar origin automaticamente. Se estiver no modelo público, explicar que ele é referência e orientar selecionar a base privada antes de preencher informações da empresa. Não criar outra base como efeito desta skill.

Confira privacidade e permissão de leitura pelo GitHub disponível. No Cloud, pode usar a ferramenta GitHub ou a API REST: `gh api repos/<proprietario>/<repositorio>` e os campos `full_name`, `private` e permissões disponíveis. Não depender de comandos gh que exigem GraphQL. Se a consulta falhar, não concluir que todo acesso Git falhou. Pedir conferência de Private na interface, se necessária, e registrar a fonte da confirmação. Sem privacidade confirmada, não registrar nem enviar dados de empresa.

A autenticação do Claude, Git e uma ferramenta GitHub pode ser diferente. Orientar login oficial, seleção da base ou aceite de convite quando faltar acesso. Não pedir credenciais, instalar Git no computador, criar CLAUDE.local.md ou prometer identificação permanente entre sessões. A pessoa pode precisar confirmar seu nome em uma sessão nova.

## Preencher com informações reais

Reutilizar o que já estiver preenchido. Perguntar somente o que faltar: nome da empresa, o que faz e para quem, pessoas e papéis. Critérios e tom podem continuar a definir. Uma segunda participante usa a mesma base e preserva os registros existentes.

Atualizar identidade.md com fonte, data e pendências. Ajustar README para apresentar a empresa, incluir o link da base privada, privacidade conferida e fontes escolhidas. Preservar a referência ao modelo e distinguir sua URL do destino de trabalho. A árvore representa a organização no repositório, não um caminho obrigatório no computador.

Não duplicar critérios nas skills nem fixar o endereço da empresa dentro de salvar. Não criar clientes, reuniões ou processos fictícios. Não manter no guia da empresa instruções de clone ou chamadas à skill de início retirada. Se a base veio de versão antiga do modelo, revisar suas instruções antes de declarar a configuração pronta, preservando alterações reais da empresa. Não apagar arquivos pessoais anteriores como efeito dessa revisão.

## Registrar, salvar e conferir

Registrar no LOG.md o trabalho real da configuração, autoria humana, IA como apoio, fontes e pendências. Na base gerada, o histórico de manutenção do modelo não é uma sessão da empresa; preservar e distinguir os registros.

Usar salvar para revisar e enviar somente estes ajustes à main da base privada conferida. Se não houver alteração real nem envio anterior pendente, não fabricar arquivo ou commit de teste: informar que esta execução não testou nova escrita.

Só confirmar conclusão depois de comprovar main remota contendo os ajustes. A configuração desta sessão não comprova o acesso de outra pessoa ou a disponibilidade dos conectores. O teste de troca exige outra sessão encontrando uma informação real na main atualizada.

## Entregar

Informar nome e link da base, documentos ajustados, resultado de leitura e salvamento em main e pendências reais. Na rotina, a pessoa começa pelo pedido de trabalho e pede para salvar ao terminar. Detalhes Git ficam com a IA e os mentores.

Esta skill não cria repositórios ou convites, altera acessos, conecta ferramentas, publica materiais, envia mensagens ou instala agendadores. Essas ações dependem de pedidos próprios.
