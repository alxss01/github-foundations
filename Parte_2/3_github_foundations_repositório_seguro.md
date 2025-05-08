### Recursos da Guia de segurança

1. No GitHub.com, acesse a página principal do repositório
2. Selecionone a opção, Segurança (Security)

**Políticas de segurança:** Na aba security, podemos adicionar um arquivo chamado `SECURITY.md` para especificar como relatar uma vulnerabilidade.

**Alertas do Dependabot:** Identifica que o repositório está usando um dependência vulnerável ou malware.

**Escaneamente do código** Para escanear o código e idenficar vulnerabilidades.

### Comunique uma política de segurança com SECURITY.md

Na aba Segurança, do repositório, você pode adicionar recursos ao seu fluxo de trabalho do GitHub para ajudar a evitar vulnerabilidades no seu repositório e na base de código. Esses recursos incluem:

- **Políticas de segurança** que permitem que você especifique como relatar uma vulnerabilidade de segurança no seu projeto adicionando um `SECURITY.md` arquivo ao seu repositório.

- **Alertas do Dependabot** que notificam você quando o GitHub detecta que seu repositório está usando uma dependência vulnerável ou malware.

- **Avisos de segurança** que você pode usar para discutir, corrigir e publicar informações sobre vulnerabilidades de segurança em seu repositório em particular.

**Escaneamento de código** que ajuda você a encontrar, selecionar e corrigir vulnerabilidades e erros em seu código.

#### Remover dados confidênciais de um repositório

https://docs.github.com/pt/authentication/keeping-your-account-and-data-secure/removing-sensitive-data-from-a-repository

### Adicionar um arquivo CODEOWNERS

Ao adicionar um arquivo `CODEOWNERS` ao seu repositório, você pode `atribuir membros individuais` da equipe ou `equipes inteiras` **como proprietários de código para caminhos no seu repositório**. Esses proprietários de código são então solicitados a revisar as solicitações de pull para quaisquer alterações nos arquivos em um caminho para o qual estão configurados.

### Sobre gráfico de dependências

https://docs.github.com/pt/code-security/supply-chain-security/understanding-your-software-supply-chain/about-the-dependency-graph

### Atualizações automatizadas de dependências com Dependabot

Um alerta de dependência pode levar um colaborador do projeto a adicionar a referência do pacote problemático à versão recomendada e criar um pull request para validação. Não seria ótimo se houvesse uma maneira de automatizar esse processo? Ótimas notícias! **O Dependabot** faz exatamente isso. Ele verifica alertas de dependência e cria pull requests para que um colaborador possa validar a atualização e mesclar a solicitação. [configurando atualizações de segurana](https://docs.github.com/pt/code-security/dependabot/dependabot-security-updates/configuring-dependabot-security-updates)

### Escaneamento secreto

Semelhante aos recursos de varredura de segurança anteriores, a varredura de segredos procura segredos ou credenciais conhecidos confirmados no repositório.

### Exercício - Proteja a cadeia de suprimentos do seu repositório

Aqui está uma recapitulação de todas as tarefas que você realizou em seu repositório:

- Você aprendeu a visualizar e usar o gráfico de dependência.
- Você aprendeu como habilitar e usar alertas do Dependabot.
- Você aprendeu como habilitar e usar as atualizações de segurança do Dependabot.
- Você aprendeu como habilitar e usar atualizações de versão do Dependabot.
  [Exercício](https://github.com/alxss01/skills-secure-repository-supply-chain/issues/1)

### Questões

1. Qual é a melhor maneira de garantir que você está integrando as versões mais seguras das dependências do seu projeto?
   R: Habilite o Dependabot para seu repositório.

2. Suponha que um dos seus projetos de código-fonte dependa de segredos mantidos em uma pasta chamada .secrets. Você gostaria de garantir que os arquivos mantidos nessa pasta nas máquinas de desenvolvimento não sejam enviados inadvertidamente para o repositório. Qual desses arquivos ajuda melhor a aplicar essa política?  
   R: .gitignore

3. O que a varredura secreta faz?
   R: Procura por segredos conhecidos ou credenciais confirmadas no repositório.
