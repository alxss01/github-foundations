# O que é administração do GitHub?

O administrador do GitHub tem como objetivo manter tudo funcionando perfeitamente para seus usuários.

### Administração em nível de equipe (Teams)

Cada usuário é um membro da organização que pode ser adicionado a uma equipe (team)

#### Melhores práticas para administração em nível de equipe

- Crie equipes aninhadas para refletir a hierarquia do seu grupo ou empresa dentro da sua organização do GitHub.
- Ajude a otimizar os processos de revisão de RP criando equipes com base em interesses ou tecnologias específicas (JavaScript, ciência de dados, etc.). Os indivíduos podem optar por participar dessas equipes de acordo com seus interesses ou habilidades.
- Habilite a sincronização de equipes entre seu IdP e o GitHub para permitir que proprietários de organizações e mantenedores de equipes conectem equipes em sua organização com grupos de IdP (Tipo Azure Entra ID).

### Administração em nível organizacional

> Recomendamos configurar apenas uma organização para seus usuários e repositórios. Se restrições específicas da sua empresa exigirem a criação de várias organizações, esteja ciente dos seguintes pontos:

- Não é possível duplicar uma organização ou compartilhar configurações entre duas organizações. Isso significa que você precisa configurar tudo do zero sempre que criar uma organização, o que aumenta o risco de erros nas suas configurações.

- Dependendo das políticas dos seus fornecedores de software, você poderá incorrer em custos extras se precisar instalar alguns aplicativos em várias organizações.

- Gerenciar múltiplas organizações é mais difícil!

#### Administração em nível empresarial (enterprise)

**No nível empresarial, os membros de uma empresa com permissões de proprietário podem:**

- Habilite o logon único da linguagem de marcação de afirmação de segurança (SAML) **_single sign-on_** para sua conta corporativa, permitindo que cada membro corporativo vincule sua identidade externa no seu IdP à sua conta GitHub existente.
- Adicione ou remova organizações da empresa.
- Configure o faturamento ou atribua um gerente de faturamento para todas as organizações da empresa.
- Configure políticas de gerenciamento de repositório, políticas do conselho do projeto, políticas de equipe e outras configurações de segurança que se apliquem a todas as organizações, repositórios e membros da empresa.
- Extraia vários tipos de informações sobre organizações por meio do uso de scripts personalizados.
- Aplique alterações em toda a empresa, como migrações, por meio do uso de scripts personalizados.

### Opções de autenticação do GitHub

1. **Nome de Usuário e Senha**

   - Nos últimos anos, a autenticação básica tem se mostrado muito arriscada ao lidar com informações altamente confidenciais

2. **Token de Acesso Pessoal**

   - Tokens de acesso pessoal (PATs) são uma alternativa ao uso de senhas para autenticação no GitHub ao usar a API do GitHub ou a linha de comando.

3. ## **Chaves SSH**

   - Ao configurar o SSH, os usuários geram uma chave SSH, adicionam-na ao ssh-agent e, em seguida, adicionam a chave à sua conta do GitHub. Adicionar a chave SSH ao ssh-agent garante que a chave SSH tenha uma senha como uma camada extra de segurança. Os usuários podem configurar sua cópia local do Git para fornecer a senha automaticamente ou podem fornecê-la manualmente sempre que usarem a ferramenta de linha de comando do Git para interagir com o GitHub.

4. **Implantar Chaves**

   - Chaves de implantação são outro tipo de chave SSH no GitHub que concede ao usuário acesso a um único repositório. O GitHub anexa a parte pública da chave diretamente ao repositório, em vez de uma conta de usuário pessoal, e a parte privada permanece no servidor do usuário. As chaves de implantação são somente leitura por padrão, mas você pode conceder a elas acesso de gravação ao adicioná-las a um repositório.

#### Opções de segurança adicionais ao GitHub

1.  **Autenticação de dois fatores**

    - A autenticação de dois fatores (2FA), também conhecida como autenticação multifator (MFA), é uma camada extra de segurança usada ao fazer login em sites ou aplicativos. Com a 2FA, os usuários precisam fazer login com seu nome de usuário e senha e fornecer outra forma de autenticação à qual somente eles têm acesso.

2.  **SSO SAML**

    - O GitHub oferece suporte limitado para todos os provedores de identidade que implementam o padrão SAML 2.0, com suporte oficial para vários provedores de identidade populares, incluindo:

      - Serviços de Federação do Active Directory (AD FS).
      - ID de entrada da Microsoft.
      - Okta.
      - UmLogin.
      - PingOne.

3.  **LDAP**

    - O Lightweight Directory Access Protocol (LDAP) é um protocolo de aplicação popular para acessar e manter serviços de informações de diretório. O LDAP permite autenticar o GitHub Enterprise Server em suas contas existentes e gerenciar centralmente o acesso ao repositório.

    **O GitHub Enterprise Server integra-se com serviços LDAP populares como:**

         - Diretório ativo.
         - Oracle Directory Server Enterprise Edition.
         - OpenLDAP.
         - Diretório aberto.

### Como funciona a organização e as permissões do GitHub?

- Permissões de repositório
- Permissões de equipe
- Permissões da organização
- Permissões empresariais

#### Níveis de permissão do repositório

**Leitura:** apenas visualização.  
**Triagem:** para quem precisa gerenciar issues e pull requests proativamente sem permissão de escrita.  
**Escrever:** recomendado para colaboradores que contribuem ativamente para o seu projeto. Escrever é a permissão padrão para a maioria dos desenvolvedores.  
**Manter:** recomendado para gerentes de projeto que precisam gerenciar o repositório sem acesso a ações sensíveis ou destrutivas  
**Administrador:** Recomendado para pessoas que precisam de acesso total ao projeto, incluindo ações sensíveis e destrutivas, como gerenciar a segurança ou excluir um repositório. Essas pessoas são proprietários e administradores do repositório.

Ponto de parada: https://learn.microsoft.com/en-us/training/modules/github-introduction-administration/4-how-github-organization-permission-works **Níveis de Permissões**
