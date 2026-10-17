# Segundo cérebro da empresa

Uma base em arquivos para guardar contexto, processos e conhecimento do trabalho. O Claude Code consulta e atualiza esses arquivos; o GitHub guarda a versão compartilhada e o histórico.

Este é um **modelo público da LÍNIA Consultoria**. A empresa usa uma base própria, privada, criada a partir dele. Cada pessoa acessa essa mesma base com sua conta, pelo Claude Code em **Cloud**. Não é necessário clonar uma pasta no computador.

## Por onde começar

| Sua situação | Próximo passo |
|---|---|
| A empresa ainda não tem uma base | Criar a base privada no GitHub a partir deste modelo e definir os convites. |
| A base já existe | Aceitar o convite, conectar GitHub ao Claude Code e selecionar a mesma base em Cloud. |
| A base está preparada | Dizer o que quer fazer. Ao terminar, pedir para salvar. |

## 1. Preparar os acessos

Cada pessoa usa sua conta GitHub e sua conta Claude com acesso ao Code. [Baixar Claude Desktop](https://claude.com/download) ou abrir [claude.ai/code](https://claude.ai/code). No desktop, escolher Cloud na aba Code.

Conectar o GitHub pelo próprio Claude e autorizar a base privada escolhida. Login e telas de autorização são concluídos pela pessoa. Uma conexão GitHub pelo Composio não substitui esse acesso do Claude Code ao repositório.

## 2. Criar uma única base privada

A primeira pessoa pode abrir este modelo no GitHub e escolher **Use this template > Create a new repository**. Definir a conta proprietária, o nome da base e a opção **Private**. Conferir a privacidade antes de preencher informações da empresa. Os mentores podem apoiar essa preparação.

Convidar a outra participante pelo GitHub, com acesso de escrita definido para o trabalho conjunto. Compartilhar a base também com os mentores quando combinado, para implementar skills de apoio e ajudar nas dúvidas. Cada pessoa aceita seu convite com a própria conta. Não compartilhar senhas.

A segunda pessoa usa a base já criada. Não cria outro repositório a partir do modelo. O repositório interno dos mentores é separado e não é entregue às participantes.

Criação e convites são etapas próprias, com destinatários e permissões definidos. As skills deste modelo não criam repositórios ou convites automaticamente.

## 3. Abrir e preparar no Cloud

Selecionar a base privada e **main** como versão de partida no Claude Code. A sessão prepara os arquivos no ambiente remoto. O Cloud pode criar uma branch interna de trabalho; a rotina de salvar leva o resultado para main.

### Primeiro preparo

Na base já selecionada, preencher e enviar:

```text
Quero preparar o segundo cérebro da minha empresa nesta base privada.

Base da empresa: <LINK_DA_BASE_PRIVADA>
Nome para o log: <COMO_QUERO_SER_IDENTIFICADA>

Leia o README, o CLAUDE.md e as regras da base. Siga configurar-cerebro.
Confira a base e a privacidade. Pergunte somente o que faltar sobre a
empresa e aproveite o que já estiver preenchido. Ao concluir, salve os
ajustes em main e confira o resultado na base compartilhada.
Não crie outro repositório, convites ou uma pasta no meu computador.
```

A skill configurar-cerebro confere o destino e o acesso, preenche identidade e mapas com informações reais e usa salvar para concluir em main. Se houver bloqueio de acesso ou conflito, preserva os arquivos e explica a pendência.

Ao concluir o preparo, a IA mostra o que entendeu sobre a empresa, os arquivos usados como fonte e o que ainda falta confirmar. Conferir esse entendimento e corrigir o que for necessário.

### Outra pessoa na mesma base

Depois de aceitar o convite e selecionar a mesma base, pode dizer:

```text
Quero trabalhar nesta base privada da empresa.

Base da empresa: <LINK_DA_BASE_PRIVADA>
Nome para o log: <COMO_QUERO_SER_IDENTIFICADA>

Leia as instruções e confira a versão atual de main. Aproveite a
identidade e os registros existentes. Quero trabalhar em: <ASSUNTO>.
```

Não há cadastro obrigatório no computador. Uma identificação confirmada vale para a sessão; se faltar evidência em uma sessão nova, a IA pode perguntar uma vez quem está trabalhando.

## 4. Usar no dia a dia

1. Abrir a base no Claude Code em Cloud, partindo de main.
2. Dizer o que quer fazer. O CLAUDE.md orienta atualizar a base e ler o contexto necessário, sem comando de início.
3. Trabalhar e conferir os arquivos utilizados como fonte.
4. Pedir “salve meu trabalho” ou usar `/salvar`.
5. Conferir a resposta: o trabalho deve estar em main, disponível para a outra pessoa.

Salvar registra os documentos e o log, recebe atualizações da outra pessoa, combina os trabalhos e confirma o resultado remoto. Enviar uma branch ou abrir um PR não é, sozinho, conclusão desse salvamento.

Se quiser retomar em outra sessão, pode pedir: “Salva e me dá um prompt para continuar em outra sessão.” A IA entrega um texto curto com objetivo, arquivos, resultado e próximo passo conhecido. O prompt só aparece quando pedido; “salva meu trabalho” mantém a confirmação curta. Não é necessário usar uma frase exata.

Se houver conflito ou acesso insuficiente, a IA preserva o resultado e informa o que falta. Nunca força o envio para sobrescrever o trabalho da outra pessoa. Uma sessão já aberta também precisa conferir atualizações antes de continuar; não é necessário ensinar comandos Git às participantes.

## 5. Conferir a troca

Uma pessoa salva uma informação real. A outra abre uma sessão na main atualizada e pede para localizar o registro. Fazer o caminho de volta. Isso confere o acesso e a recuperação, sem exigir cópias locais nos computadores.

Ainda é necessário testar esse comportamento no Claude Cloud e com as contas que usarão a base. O arquivo de uma skill e a documentação do ambiente não comprovam sua execução.

## Estrutura

```text
base-da-empresa/
  README.md
  contexto-da-empresa/
    identidade.md
    produtos-servicos-e-entregas.md
    clientes-e-mercado.md
    pessoas.md
    comunicacao-e-referencias.md
  AGENTS.md
  CLAUDE.md
  LOG.md
  .gitignore
  clientes/
    README.md
  processos/
    mapa-dos-processos.md
  .claude/
    skills/
      configurar-cerebro/
        SKILL.md
      salvar/
        SKILL.md
```

| Local | O que guardar |
|---|---|
| [contexto-da-empresa/](contexto-da-empresa/identidade.md) | Cinco áreas: identidade, ofertas, clientes e mercado, pessoas e comunicação. |
| [clientes/](clientes/README.md) | Contexto, fontes e particularidades de clientes reais. |
| [processos/](processos/mapa-dos-processos.md) | Mapa macro de jornada, back office e rotinas. Documentação detalhada entra conforme a necessidade. |
| [LOG.md](LOG.md) | Data, autoria, trabalho, resultado e pendências de cada sessão. |
| [CLAUDE.md](CLAUDE.md) | Início automático, leitura de contexto e conferência da base. Importa as regras gerais. |
| [AGENTS.md](AGENTS.md) | Onde guardar, como revisar, registrar e preservar o trabalho. |
| [.claude/skills/configurar-cerebro/](.claude/skills/configurar-cerebro/SKILL.md) | Preparar ou retomar a base privada. |
| [.claude/skills/salvar/](.claude/skills/salvar/SKILL.md) | Registrar e concluir o salvamento em main. |

Os arquivos de contexto são pontos de partida, preenchidos aos poucos. A IA mantém fontes, datas e uma referência principal, seguindo o AGENTS.md. Não criar pastas vazias ou documentos adicionais apenas para completar a árvore.

As skills de tarefas reais podem ser acrescentadas conforme o uso. Consultam processos e contexto sem manter cópias concorrentes dos critérios.

## Fontes e conexões da empresa

Preencher somente com fontes escolhidas e acessos reais. Não guardar credenciais.

| Fonte ou ferramenta | O que contém | Link ou localização | Acesso e teste |
|---|---|---|---|
| A definir | A definir | A definir | Não configurado |

Tarefas atuais, agenda, planilhas operacionais e gravações continuam no sistema de origem. Registrar o link e o papel de cada fonte. Fontes de um cliente ficam no README dele.

As outras ferramentas podem conectar pelo Composio remoto no Claude. Cada pessoa autoriza seu acesso e confere uma consulta na sessão Cloud. Compartilhar arquivos não compartilha automaticamente as conexões. Conectar uma ferramenta não agenda uma automação.

## Sobre este modelo

Criado em 11/10/2026 para a mentoria de segundo cérebro e IA da LÍNIA. Revisado em 14/10/2026: início pelas instruções, preparação no Cloud e salvamento com destino main. Revisado em 17/10/2026: contexto separado por áreas, mapa de processos nomeado e organização, fontes e atualização atribuídas à IA. A [manutenção no log](LOG.md#manutenção-do-modelo) registra a origem e os limites de teste; não é histórico de uma empresa.

Uma base gerada tem vida própria. Revisões futuras deste modelo não atualizam automaticamente a base da empresa; revisar a adaptação preservando seu conteúdo.

**Fontes técnicas, consultadas em 14/10/2026:** [início no Cloud](https://code.claude.com/docs/en/web-quickstart), [ambiente e proxy GitHub](https://code.claude.com/docs/en/cloud-environments#github-proxy), [instruções do Claude](https://code.claude.com/docs/en/memory), [skills no Cloud](https://code.claude.com/docs/en/skills#use-skills-in-cowork-and-cloud-sessions), [criar a partir de modelo](https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-repository-from-a-template) e [Composio remoto](https://composio.dev/toolkits/composio/framework/claude-cowork).
