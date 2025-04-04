# Configurar a varredura de código no GitHub
* Serviço de varredura de código para verificar existência de vulnerabilidades.

## O que é varredura/digitalização/scanning de código?
* A varredura de código usa o CodeQL para analisar o código em um repositório do GitHub para encontrar vulnerabilidades de segurança e erros de codificação. 
* A varredura de código está disponível para todos os repositórios públicos e para repositórios privados de propriedade de organizações onde o GitHub Advanced Security está habilitado.
* Você pode agendar varreduras para determinados dias e horários, ou disparar varreduras quando um evento específico ocorrer no repositório, como um push.

## Scanning de código com CodeQL
* CodeQL é o mecanismo de análise de código que o GitHub desenvolveu para automatizar verificações de segurança.
* Há três maneiras principais de configurar a análise de CodeQL para varredura de código:
    * **Padrão**: Esta opção de configuração executa a varredura de código manualmente. Escolha da linguagem, conjunto de consultas para verificar, etc. Executa a varredura como uma GitHub Actions.
    * **Avançada**: Fluxo de trabalho personalizável, que usa o github/codeql-action
    * **CLI**: Execute o CodeQL CLI diretamente em um sistema de CI externo e carregue os resultados no GitHub.
* O CodeQL oferece suporte a linguagens compiladas e interpretadas e pode encontrar vulnerabilidades e erros em códigos

## Habilitar o CodeQL no repositório com a configuração padrão.
* Repositório >> Security >> Code Scanning Alerts >> Padrão/Default
* Executar a varredura de código com GitHub Actions afeta seus minutos de cobrança mensal. Se você quiser usar GitHub Actions além do armazenamento ou minutos incluídos em sua conta, você será cobrado por mais uso.


## Habilitar varredura/scanning de código com ferramentas de terceiros.
* Você pode carregar arquivos Static Analysis Results Interchange Format (SARIF) gerados fora do GitHub ou com GitHub Actions para ver alertas de varredura de código de ferramentas de terceiros no seu repositório.
* Fazer o exemplo do último workflow com ESLint com output result.sarif: https://learn.microsoft.com/en-us/training/modules/configure-code-scanning/3-enable-code-scanning-with-third-party-tools

## Configurar varredura/scanning de código.
* Como discutimos nas unidades anteriores, você pode executar a varredura de código no GitHub, usando GitHub Actions ou do seu sistema de integração contínua (CI). 
* Mudar verredura de código de padrão para avançada: Settings >> security analysis (Advanced Security) >> (...) >> switch Advanced. Editar o Workflow aberto.
* As varreduras podem ser configuradas para serem executadas de tempos em tempos ou após determinado evento como `on:push`, `on:pull_request[open]`.
* Se você fizer a varredura no push, os resultados aparecerão na aba Segurança do seu repositório
* Definir severidade que causam falha de vulnerabilidade: Error, Critical, High
* Falhas de solicitação de pull não interrompem uma varredura de código, mas representam um bloqueador ao tentar mesclar (merge) código.
* Severidade: Settings >> Advanced Security >> Protection rules (Mudar severidade) High or higher
* Repositório para exercícios: https://github.com/skills/introduction-to-codeql (Verificar como é configurado botões no README)
* O Code Scanning faz parte do conjunto de produtos GitHub Advanced Security (GHAS) . Todos os recursos do Advanced Security são 100% gratuitos para repositórios públicos de código aberto.

Ponto de parada:
* Fazer Exercício: https://github.com/skills/introduction-to-codeql