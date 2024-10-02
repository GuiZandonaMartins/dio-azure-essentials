## Ferramentas de gerenciamento e implantação 

A Azure oferece algumas opção de ferramentas para implantar os recursos no ambiente, são elas:

- Portal da Azure: O portal padrão da Azure com uma interface gráfica para fazer todo o gerenciamento do seu ambiente.

- Azure Cloud Shell: Uma interface via linha de comando disponível dentro do portal da Azure que permite fazer a criação dos recursos utilizando apenas comandos. Possui a opção de utilizar o PowerShell ou o CLI, com a implantação via código é possível fazer a configurações do ambiente em massa rapidamente.

- ARM (Azure Resource Manager): É uma camada de gerenciamento que recebe as requisições e faz a administrações dos recursos, criando ou alterando o que foi solicitado. Os modelos do ARM são no formato JSON (Java) e podem ser utilizados para criar e implantar a infraestrutura sem precisar criar um novo código.

- Bicep: É uma linguagem de programação criada pela Microsoft, sendo compatível somente com a nuvem da mesma.

## Azure Arc

É utilizado para fazer o gerenciamento de recursos fora da nuvem da Azure, seja no ambiente local ou em outros provedores (AWS, GCP).

Possui um painel único para o gerenciamento, utilizando todas as práticas nativas da nuvem e com um controle de acesso baseado em função, garantindo a segurança e confiabilidade.

## Links Úteis

- Calculadora: https://azure.microsoft.com/pt-br/pricing/calculator/

- Calculadora TCO: https://azure.microsoft.com/pt-br/pricing/tco/calculator/

- Verificação de Status: https://azure.status.microsoft/pt-br/status

- Curso gratuito da Microsoft: https://learn.microsoft.com/pt-br/credentials/certifications/azure-fundamentals/?practice-assessment-type=certification
