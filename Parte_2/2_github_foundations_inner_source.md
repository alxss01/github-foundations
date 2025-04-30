# Gerenciar Programa Inner Source no GitHub

### Software Aberto

- O software de código aberto se beneficiava de sua característica de abertura: qualquer pessoa pode contribuir, e muitas pessoas o fazem.

### Software Proprietário

- O software proprietário, por outro lado, limita o acesso por meio de um sistema fechado que preza a privacidade de sua propriedade intelectual (PI).

### O que é InnerSource?

**InnerSource** é a prática de aplicar padrões de código aberto a projetos com um público limitado. Por exemplo, uma empresa pode estabelecer um programa InnerSource que espelhe a estrutura de um projeto de código aberto típico, exceto que seja **acessível apenas aos funcionários dessa empresa**. Na prática, **é um programa de código aberto protegido pelo firewall da sua empresa.**

## Configurar um programa InnerSource no GitHub

Repositórios com 3 níveis de visibilidade

1.  Públicos: Opção de acesso para pessoas dentro e fora da sua organização.
2.  Internos: Visíveis apenas para membros da organização que os possui. Use essa visibilidade para projetos InnerSource.
3.  Privados: Visíveis apenas por proprietários e equipes e membros que ele adiciona. Use quando apenas grupos específicos podem ter acesso.

### Permissões individuais ou de equipes

- Leitura (read): Para colaboradores que precisam visualizar ou discutir o projeto.
- Triagem (triage): Para colaboradores que precisam gerenciar problemas e pull request proativamente sem acesso de gravação.
- Escrita (write): Para colaboradores que contribuem ativamente para o projeto.
- Manter (Maintain): Para gerentes de projeto que precisam gerenciar o repositório sem acesso a ações sensíveis ou destrutivas.
- Administrador (Admin): Para colaboradores que precisam de acesso total ao projeto, incluindo ações sensíveis e destrutivas, como gerenciar a segurança ou exluir um repositório.

### Arquivo README

Um arquivo readme comunica a expectativa para o projeto.
User recursos visuais, como imagens das telas, links que demonstre a versão em produção.

- Exemplo de readme's incriveis: https://github.com/matiassingers/awesome-readme?tab=readme-ov-file

### Gerenciar Projetos no GitHub

`CONTRIBUTING.md` arquivo na raiz (ou /docs ou /.github) de um repositório. Use esse arquivo para explicar a política de contribuição do projeto.

- Exemplos incríveis de `contributing.md`: https://github.com/mntnr/awesome-contributing

### Modelos de problemas e Pull Request

Por exemplo, se o seu projeto tiver `.github/ISSUE_TEMPLATE.md` ou `.github/PULL_REQUEST_TEMPLATE.md`, sempre que um usuário iniciar o processo de criação de um problema, ele verá este conteúdo.

- Exemplos incríveis de modelos de Issues e Pull Request: https://github.com/devspace/awesome-github-templates

### Definir fluxos de trabalho

O fluxo de trabalho deve incluir detalhes sobre onde e como as branches devem ser usadas para bugs e funcionalidades

### Perguntas

1.  Qual das seguintes opções descreve melhor a relação entre os programas de código aberto e InnerSource ?
    R: Os programas da InnerSource são fundamentalmente os mesmos que os programas de código aberto, exceto que seu acesso é limitado às pessoas dentro da organização.

2.  Suponha que sua equipe esteja recebendo relatórios de bugs de baixa qualidade, sem informações suficientes para um diagnóstico adequado. Qual das seguintes opções é a melhor maneira de resolver o problema?
    R: Adicione um ISSUE_TEMPLATE.mdarquivo que inclua campos para etapas de reprodução, propriedades do sistema e instruções para gerar e incluir logs importantes.

3.  Suponha que sua equipe esteja monitorando dados de todos os tipos desde que seu programa InnerSource foi lançado há três meses. Qual das seguintes métricas indica que seu programa é um grande sucesso?
    R: Um aumento drástico nas solicitações de pull que corrigem bugs no seu software.
