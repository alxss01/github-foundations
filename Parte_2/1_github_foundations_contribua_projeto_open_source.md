# Contribuir para um projeto de código aberto.

### Contribuir em projetos usados diariamente

1. Podemos contribuir para projetos de código aberto usados diariamente, talvez uma biblioteca que usamos em Java, Python ou NodeJS.

### Busca no GitHub

1. Podemos usar a pesquisa do GitHub para explorar tópicos e projetos por palavra-chave: https://github.com/search

2. Pesquisar por machine learning, por exemplo, irá carregar tudo relacionado a palavra-chave em questão.

3. Podemos restringir a pesquisa por tópicos, usando o menu lateral do lado esquerdo.

4. Começar a contribuir seja com código-fonte, documentação, correção ortagráfica, etc.

### Familiarize-se com um projeto de código aberto

1. Documentos no nível superior do repositório:

   1. Licença: Deverá conter uma licença de código aberto. Se não houver licença, não é de código aberto.
   2. Readme: Página de boas-vindas. Fornece informações de como começar a usar o projeto.
   3. Contribuindo: Fornece orientações de como contribuir para o projeto e detalhes de como montar o ambiente de desenvolvimento.
   4. Código de conduta:Regras básicas para os membros da comunidade.

2. Familiarizar com a comunidade, alguns canais:
   1. Verificar issues: Tarefas e melhorias relacionadas ao projeto.
   2. Pull requests: Discussão e revisão das alterações no projeto.
   3. Canais de bate-papo e fóruns: Slack, Gitter e IRC

### Identificar tarefas para trabalhar

1. Uma boa maneira de encontrar problemas para iniciantes é vistar a /contribute, por exemplo: https://github.com/jupyter/notebook/contribute

2. Acessar as [labels](https://github.com/jupyter/notebook/labels) e verificar rótulos como `help wanted`, `discussion`

### Patrocine um projeto.

1. Se um projeto for elegível para patrocínio por meio do GitHub Sponsors, você encontrará um botão (ícone de coração) Patrocinador na página principal do projeto.

## Contribuir para um repositório de código aberto

1. Passos para iniciar a contribuição

   1. Comunique a intenção aos mantenedores.
   2. Verificar se ninguém está atribuído a issue que deseja trabalhar, consultando a seção **Responsáveis**. Verifique também **Pull Request** vinculada, que significa que já tem alguém trabalhando nela.
   3. Tudo estando claro, ou seja, ninguém estiver trabalhando na issue em questão, publique um comentário sobre a issue para indicar o interesse.
   4. Exemplo de ninguém trabalhando em determinada issue:

      ![alt text](images/issue_disponivel.png)

2. Passos práticos
   1. Criar fork do repositório
   2. Fazer clone na máquina local `git clone <URL>`.
   3. Criar nova branch `git checkout -b feature/validate`
   4. Realizar ajustes, fazer commit e push
   5. Abrir PR, respeitando as boas práticas descritas no arquivo CONTRIBUTING.md, especificando a Issue que foi trabalhada.
   6. Caso alteração ainda esteja em andamento, poderá ser criada draft pull request (rascunho para pedir orientação)

### Criando Pull Requests

- Para descrever boas mensagens de commit

  1.  O assunto da mensagem de commit deve completar a seguinte frase

      - Se aplicado, esse commit irá <...>

  2.  Descrição sucinta usando o imperativo, presente do indicativo.

      - Adiciona/adicionado (add/added) método de validação de data e hora

  3.  Limite o **assunto** a 50 caracteres.

  4.  Comece com letra maiúsca e não termine com ponto final (.)

  5.  Na mensagem de Pull Request, use sempre o tempo presenta

      - Certifique-se de incluir a motivação da mudança.
      - Explicar o quê e porquê, não o como.

### Exercício

- Fork -> clone -> edit -> PR que você encontrará frequentemente como contribuidor!
  https://github.com/firstcontributions/first-contributions/blob/main/docs/translations/README.pt_br.md

- Se você quiser mais prática, verifique code [contributions](https://github.com/roshanjossey/code-contributions).

- Problemas simples que você pode começar. Verifique em [a lista de projetos no web app](https://firstcontributions.github.io/#project-list)

### Usando formattador de código?

- Se tiver usando formatador de código, usar `git add -p`

### Perguntas

1. Qual é o melhor lugar em um repositório do GitHub para descobrir onde você pode ajudar em um projeto?
   R: The Issues List (A lista de problemas)

2. Qual é a maneira preferida de pedir ajuda ou avaliações em uma pull request?
   R: Adicionar comentário na pull request.

3. O que é necessário antes de criar uma solicitação de pull no GitHub?
   R: Fork um repositório, Clone, commit das alterações, e push para o meu fork.
