# O que é controle de versão?
* Um sistema de controle de versão (VCS) é um programa ou conjunto de programas que rastreia alterações em uma coleção de arquivos.
* Outro nome para um VCS é um sistema de gerenciamento de configuração de software (SCM). 

* Anexe uma tag a uma versão, por exemplo, para marcar um novo lançamento.

# Terminologia Git
* Repositório: Um repositório bare é geralmente um diretório com um nome que termina em .git —por exemplo, project.git  
* Hash: Um número produzido por uma função hash que representa o conteúdo de um arquivo ou outro objeto como um número fixo de dígitos.
* Objeto : Um repositório Git contém quatro tipos de objetos, cada um identificado exclusivamente por um hash SHA-1. Um objeto blob contém um arquivo comum. Um objeto tree representa um diretório; ele contém nomes, hashes e permissões. Um objeto commit representa uma versão específica da árvore de trabalho. Uma tag é um nome anexado a um commit.
* Branch : Um branch é uma série nomeada de commits vinculados. O commit mais recente em um branch é chamado de head. O head do branch atual é chamado de HEAD.
* Remoto : Um remoto é uma referência nomeada para outro repositório Git. Quando você cria um repositório, o Git cria um remoto chamado originque é o remoto padrão para operações push e pull.
* Comandos , subcomandos e opções: 
    * git (comando); commit (subcomando); -m (operação)
    * git (comando); config (subcomando); --global (operação)
    * git (comando); config (subcomando); --list (operação) 

# Git e GitHub
* Git é um sistema de controle de versão distribuído (DVCS) que vários desenvolvedores e outros colaboradores podem usar para trabalhar em um projeto. Ele fornece uma maneira de trabalhar com uma ou mais ramificações locais e, então, enviá-las para um repositório remoto.
* O GitHub é uma plataforma de nuvem que usa o Git como sua tecnologia principal. O GitHub simplifica o processo de colaboração em projetos e fornece um site, mais ferramentas de linha de comando e fluxo geral que desenvolvedores e usuários podem usar para trabalhar juntos.
## Os principais recursos fornecidos pelo GitHub incluem:
* Issues
* Discussions
* Pull Requests
* Notificações
* Labels
* Actions
* Forks
* Projetos

# Prática:
1. Necessário para os commits: `git config --global user.name` "Alex" && `git config --global user.email` "alexdesouzasilva94@gmail.com"
2. Crie uma pasta chamada `cats`. Esta pasta será o diretório do projeto, também chamado de árvore de trabalho.
3. Inicia o repositório e define a branch main: `git init -b main`
4. Mostrar status da árvore de trabalho: `git status` (demonstrará alterações e ramificação/branch atual)

* A pasta .git armazena metadados e histórico para árvore de trabalho. Git atualiza os metadados lá conforme o status da árvore de trabalho muda para manter o controle do que foi alterado em seus arquivos.

# Obtendo ajuda do Git
* `git --help`:  branch List, create, or delete branches

# Comandos básicos do Git
* `git switch feature/revision`: mudando de branch.
* `git status` exibe o estado da árvore de trabalho e da área de preparação. Permite verificar quais alterações estão sendo rastreadas pelo Git no momento.
* `git add` comando usado para dizer ao git para começar a monitorar as alterações. O termo técnico é ***staging*** essas mudanças. Mudanças para se preparar para um commit. **Todas mudanças que foram adicionadas mas ainda não foram commitados, são armazenados na staging area**.
* `git commit` Commit é um verbo e um substantivo. Como verbo, fazer commit de mudanças significa que você coloca uma cópia (do arquivo, diretório ou outra "coisa") no repositório como uma nova versão. Como substantivo, um commit é o pequeno pedaço de dados que dá às mudanças que você fez commit uma identidade única. Os dados que são salvos em um commit incluem o nome e endereço de e-mail do autor, a data, comentários sobre o que você fez (e por quê), uma assinatura digital opcional e o identificador único do commit anterior.
* `git log` comando permite verificar informações de commits anteriores. o git logcomando imprime informações sobre os commits mais recentes, como seu carimbo de data/hora, o autor e uma mensagem de commit. Este comando ajuda você a manter o controle do que você tem feito e quais alterações foram salvas.
* `git help` cada comando vem com sua própria página de ajuda. Ex.: `git commit --help`

**A colaboração com outros desenvolvedores é onde o controle de versão brilha.**
