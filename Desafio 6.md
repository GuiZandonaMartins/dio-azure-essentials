## Segurança

A parte de segurança trabalha com o conceito confiança zero e de defesa em profundidade, montando várias camadas de defesa para o acesso aos dados, com o objetivo de retardar o avanço de uma possível invasão e evitar o acesso indevido as informações armazenadas.

- Autenticação x Autorização

	- Autenticação: É a confirmação de que as credenciais informadas estão corretas.

	- Autorização: Determina o nível de acesso do usuário, definindo quais recursos ou informações o usuário terá cesso.

- Microsoft Entra ID: É o serviço de gerenciamento de identidades, validando suas credenciais durante o acesso as aplicações. Ele garante a autenticação dos usuários, o logon único (SSO e o gerenciamento de aplicativos e dispositivos.

- Microsoft Entra Domain Services: Faz sincronização dos usuário do serviço de AD local para o Entra ID na Azure. Ao criar um novo usuário no AD local o mesmo é replicado para o serviço na nuvem permitindo a autenticação nos dois ambientes.

Microsoft Entra External ID: Possibilita que usuário externos façam o acesso ao seu ambiente de forma confiável ou aplicação, através de contas confiáveis como a conta do Google.

- Autenticação Multifator: Garante uma segurança adicional, solicitando elementos adicionais para a autenticação, como digitar um código ou inserir um Smartcard.

- Acesso Condicional: Faz o monitoramento das informações do usuário durante o acesso, permitindo ou não o acesso em determinadas situações.

- Controle de acesso baseado em função: É possível gerenciar cada recurso que o usuário terá acesso, garantindo que acesso somente os recursos necessário para fazer o trabalho. A permissão de acesso a recurso é herdada para os serviços que estão abaixo dele, Exemplo: ao dar permissão de acesso ao usuário em um grupo de recursos, o mesmo terá acesso a todos os recursos que estão abaixo deste grupo.

- Microsoft Defender para a nuvem: É um serviço que monitora e fornece proteção contra ameaças nos datacenters da Azure e locais, fornece também sugestões de correções para os problemas apresentados. Este serviço possui comunicação com a AWS e GCP, conseguindo apontar problemas fora do ambiente da Microsoft.
 
---Links Úteis---

Calculadora- https://azure.microsoft.com/pt-br/pricing/calculator/

Verificação de Status- https://azure.status.microsoft/pt-br/status

Curso gratuito da Microsoft- https://learn.microsoft.com/pt-br/credentials/certifications/azure-fundamentals/?practice-assessment-type=certification
