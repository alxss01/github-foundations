# GitHub Codespaces

## Ciclo de vida
* O ciclo de vida de um Codespace começa quando você cria um Codespace e termina quando você o exclui

## Criar um Codespace
* Um codespace pode ser criado no GitHub.com, no VSCode, ou pelo GitHub CLI.
* Há 4 maneiras de criar um Codespace:
    1. De um tamplate do GitHub ou de qualquer repositório de templates no GitHub.com para iniciar um novo projeto.
    2. De uma branch no repositório, para novos recursos.
    3. De uma PR aberta para explorar o trabalho em andamento.
    4. De um commit no histórico de um repositório para investigar um bug em um momento específico.
* Pode-se criar mais de um Codespace por repositório ou mesmo por branch.
* Há limites para o número de Codespaces que pode ser criado e executado ao mesmo tempo.
* Tempo de inatividade que fará stop automático do namespace: 30 min (o tempo pode ser customizado)
* Tempo de inatividade que excluirá o codespace automaticamente: 30 dias (pode ser personalizado)

> Você pode criar um número ilimitado de Codespaces por repositório ou branch, dependendo do espaço disponível. Ao atingir um limite de recursos, uma mensagem será exibida informando que um Codespace existente precisa ser removido/excluído antes que um novo Codespace possa ser criado.

## Personalize o Codespace
* **Sincronização de configurações:** você pode sincronizar as configurações do Visual Studio Code (VS Code) entre o aplicativo de desktop e o cliente web do VS Code.
* **Dotfiles:** Você pode usar um repositório dotfiles para especificar scripts, preferências de shell e outras configurações.
* **Alterar o tipo de máquina:** você pode alterar o tipo de máquina que está executando seu Codespace para usar recursos apropriados para o trabalho que está fazendo.
* **Definir o editor padrão:** Visual Studio Code, JetBrains Gateway, JupyterLab
* **Definir a região padrão:** você pode definir sua região padrão na página de configurações de perfil do GitHub Codespaces **para personalizar onde seus dados são armazenados**.

## Codespaces vs editor GitHub.dev
> Você pode usar o GitHub.dev para navegar por arquivos e repositórios de código-fonte do GitHub, além de fazer e confirmar alterações no código. Você pode abrir qualquer repositório, fork ou pull request no editor do GitHub.dev.

> Se você quiser fazer trabalhos mais pesados, como testar seu código, use o GitHub Codespaces. Ele tem computação associada para que você possa compilar seu código, executá-lo e ter acesso ao terminal. O GitHub.dev não possui computação. Com o GitHub Codespaces, você obtém o poder de uma Máquina Virtual (VM) pessoal com acesso ao terminal, da mesma forma que usaria seu ambiente local, só que na nuvem.

## Mais detalhes:
* https://github.blog/2023-02-22-a-beginners-guide-to-learning-to-code-with-github-codespaces/
* https://docs.github.com/en/codespaces/developing-in-codespaces/developing-in-a-codespace
* https://docs.github.com/en/codespaces/customizing-your-codespace

