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

**Podemos criar modelo de repositório, para que todo repositório criado a partir do modelo já tenha as configurações de permissões padronizadas.**

1. Em GitHub.com, acessar página do repositório.
2. Na página do repositório >> settings >> Selecionar repositório de modelo.

#### Formas pelas quais usuários recebem acesso ao repositório

| Tipo de Associação              | Descrição                                                                                                                 |
| ------------------------------- | ------------------------------------------------------------------------------------------------------------------------- |
| Colaborador direto              | Adicionado explicitamente ao repositório com uma função específica (leitura, triagem, escrita, manutenção, administração) |
| Membros da equipe               | Usuário herda o acesso ao repositório por meio de sua associação à equipe (Team)                                          |
| Permissão padrão da organização | Se o repositório fizer parte de uma organização, pode haver um nível de permissão padrão para todos da organização        |
| Colaborador Externo             | Um usuário que não é membro da organização, mas tem acesso explícito a um repositório (terceiros, freelancers)            |

**Dica:** Sempre siga o Princípio do Menor Privilégio — atribua o menor nível de permissão necessário para que cada equipe execute suas tarefas com eficiência. Essa abordagem reduz o risco de alterações acidentais ou não autorizadas.

### Gerenciando acesso empresarial, permissões e governança

#### Existem vários níveis de permissões no nível organizacional:

**Proprietário:** Os proprietários da organização podem fazer tudo o que os membros da organização fazem, além de adicionar ou remover outros usuários da organização. Essa função deve ser limitada a, no mínimo, duas pessoas na sua organização.

**Membro:** Os membros da organização podem criar e gerenciar repositórios e equipes da organização.

**Moderador:** Os moderadores da organização podem bloquear e desbloquear colaboradores não membros, definir limites de interação e ocultar comentários em repositórios públicos de propriedade da organização.

**Gerente de cobrança:** Os gerentes de cobrança da organização podem visualizar e editar informações de cobrança.

**Gerentes de segurança:** Os gerentes de segurança da organização podem gerenciar alertas e configurações de segurança em toda a sua organização. Eles também podem ler permissões para todos os repositórios da organização.

**Colaborador externo:** Colaboradores externos, como consultores ou funcionários temporários, podem acessar um ou mais repositórios da organização. Eles não são membros explícitos da organização.

#### Níveis de permissão empresarial

Lembre-se de que contas corporativas são conjuntos de organizações. Por extensão, cada conta de usuário individual que é membro de uma organização também é membro da empresa. Você pode controlar diversas configurações relacionadas à autenticação a partir deste nível superior.

**Existem três níveis de permissão no nível empresarial:**

1. Proprietário

Os proprietários da empresa têm controle total sobre a empresa e podem tomar todas as medidas, incluindo:

- Gerenciar administradores.
- Adicionar e remover organizações da empresa.
- Gerenciar configurações da empresa.
- Aplicar políticas em todas as organizações.
- Gerenciar configurações de cobrança.

2. Membro

Os membros da empresa têm o mesmo conjunto de habilidades que os membros da organização.

3. Gerente de cobrança

Os gerentes de cobrança empresarial só podem visualizar e editar as informações de cobrança da sua empresa e adicionar ou remover outros gerentes de cobrança.

4. Colaborador convidado

Pode receber acesso a repositórios ou organizações, mas tem acesso limitado por padrão (somente usuários gerenciados pela empresa)

**Para otimizar ainda mais o controle de acesso em escala empresarial:**

- **Equipes aninhadas:** contas corporativas podem usar estruturas de equipes aninhadas para refletir hierarquias departamentais. As permissões de uma equipe principal são transferidas em cascata para equipes secundárias, simplificando o gerenciamento complexo de acessos.

- **Automação e auditoria:** você pode usar a API do GitHub ou o GitHub Actions para automatizar a criação de equipes e atribuições de permissões, além de auditar o acesso por meio de logs de auditoria da organização ou da empresa.

### Pesando os prós e os contras de implantar uma única organização ou várias organizações

1. Organização Única

   - **Gerenciamento simplificado:** controle centralizado de permissões e políticas.

2. Várias organizações

   - **Políticas personalizadas:** personalize as permissões para atender às necessidades específicas de cada equipe.

#### Sincronização de equipe através do Active Directory (AD)

Usar o Active Directory (AD) para sincronização de equipe torna o gerenciamento de usuários e o controle de acesso mais fáceis e eficientes.

##### Por que usar a sincronização do AD?

- Fonte única de verdade: mantém as identidades dos usuários consistentes em toda a sua organização.
- Gerenciamento de acesso automatizado: simplifica a integração, o desligamento e as atualizações de funções.
- Alinhamento perfeito de funções: garante que os grupos do AD correspondam às funções e permissões da empresa.

#### Manutenibilidade: scripts para múltiplas organizações e direitos de acesso

À medida que sua empresa cresce, automatizar o gerenciamento de permissões em várias organizações é essencial para a manutenção.

**Modularidade:** Desenvolva scripts em componentes modulares para lidar com diferentes organizações com alterações mínimas.
**Reutilização:** crie funções ou módulos reutilizáveis para executar tarefas de permissão comuns.
**Teste:** teste completamente os scripts em um ambiente controlado antes da implantação.
**Registro:** implemente registro detalhado para rastrear alterações e facilitar a solução de problemas.
**Controle de versão:** use sistemas de controle de versão (como o Git) para gerenciar revisões de script e colaborar com os membros da equipe.

## Questões:

1. Você deseja conceder a um usuário as permissões necessárias para adicionar e remover membros da organização de uma equipe. Qual permissão você precisa conceder a esse usuário?
   **R: Mantenedor da equipe**

2. Como proprietário de uma organização, você quer garantir que todos que estiverem conectados à sua rede corporativa possam acessar o site do GitHub sem precisar de um segundo login. Qual tecnologia você habilitaria para isso?
   **R: Login único**

3. Qual é o nível de permissão de repositório apropriado para colaboradores que precisam enviar ativamente alterações para seu repositório?
   **R: Escrever**

4. Qual função dentro de uma equipe pode adicionar ou remover membros da equipe?
   **R: Mantenedor de equipe**

5. Qual nível de permissão é melhor para gerentes de projeto que precisam selecionar e organizar problemas sem contribuir com código?
   **R: Triagem**

6. Qual é o benefício de integrar o Active Directory (AD) para sincronização de equipe?
   **R: Gerenciamento de identidade centralizado**

7. Qual das seguintes ações é exclusiva para Proprietários de Organização no GitHub?
   **R: Gerenciar configurações da organização, incluindo segurança e cobrança**

8. Qual é a principal diferença entre um membro da organização e um colaborador externo?
   **R: Os membros da organização são incluídos no diretório interno da organização.**

9. Qual nível de permissão permite que os usuários gerenciem as configurações do repositório, mas não excluam ou transfiram o repositório?
   **R: Manter**
