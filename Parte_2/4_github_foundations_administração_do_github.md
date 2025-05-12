# O que é administração do GitHub?

O administrador do GitHub tem como objetivo manter tudo funcionando perfeitamente para seus usuários.

### Administração em nível de equipe (Teams)

Cada usuário é um membro da organização que pode ser adicionado a uma equipe (team)

#### Melhores práticas para administração em nível de equipe

- Crie equipes aninhadas para refletir a hierarquia do seu grupo ou empresa dentro da sua organização do GitHub.
- Ajude a otimizar os processos de revisão de RP criando equipes com base em interesses ou tecnologias específicas (JavaScript, ciência de dados, etc.). Os indivíduos podem optar por participar dessas equipes de acordo com seus interesses ou habilidades.
- Habilite a sincronização de equipes entre seu IdP e o GitHub para permitir que proprietários de organizações e mantenedores de equipes conectem equipes em sua organização com grupos de IdP (Tipo Azure Entra ID).

#### Administração em nível organizacional

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

// Ponto de parada: https://learn.microsoft.com/en-us/training/modules/github-introduction-administration/3-how-github-authentication-works
