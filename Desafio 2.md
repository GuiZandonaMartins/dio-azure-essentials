# Criação de Banco de Dados na Azure
 
 
 ## 1.Acesse o portal da Azure

- Acesse o [portal da Azure](portal.azure.com) e efetue o login.

## 2. Ir até o serviço de bancos de dados

- No menu esquerdo, selecione Bancos de Dados SQL .

- Clique em Criar.

## 3. Escolher a assinatura e o grupo de recursos

- Selecione a assinatura que deseja utilizar para criar o Banco de dados.

- Escolha um grupo de recursos existente ou crie um novo.

	*Com o grupo de recursos é possível organizar e gerenciar os recursos relacionados.*

## 4. Defina os detalhes do banco de dados

- Nome do banco de dados: Defina o nome do banco de dados.

- Servidor SQL: É possível selecionar um servidor existente ou criar um novo.

<details>
<summary>Para a criação de um novo servidor</summary>
  
**Criação de novo servidor**
  
  1. Nome do servidor: Defina um nome para o servidor (deve ser exclusivo globalmente).
  
  2. Região: Escolha a região onde o servidor será implantado.
  
  3. Autenticação: Defina se a autenticação será feita via Microsoft Entra, autenticação SQL ou ambos.
  
  4. Definir Administrador: Defina o usuário que será o administrador do servidor.
  
</details>

- Elastic Pools: Se necessário, pode optar por adicionar o banco de dados a um Elastic Pool, que permite compartilhar recursos entre vários bancos de dados.

- Ambiente: Defina se seu ambiente é de Desenvolvimento ou Produção.
  
- Configurações de backup: Selecione o tipo de redundância que será utilizada para armazenar seu Backup.

<details>
<summary>Detalhes</summary>
  
 - Redundância local: É feita a replicação dos dados dentro de um mesmo Datacenter.
 - Redundância de Zona: É feita a replicação dos dados distribuídos por zonas geográficas diferentes.
 - Redundância Geográfica: É feita a replicação dos dados em zonas geográficas diferentes.
 - Redundância de zona geográfica: É feita a replicação dos dados em duas regiões diferentes  e dentro destas zonas, em datacenters diferentes.
</details>

## 6. Rede

- Acesso à rede: Defina se o acesso  ao banco de dados será público ou restrito a redes específicas.

## 7. Revise todas as configurações

- Revise todas as configurações e clique em Revisar e Criar, após a validação clique em Criar e aguarde o processo de criação.

## 8.Conectar ao banco de dados

- Após a criação, é possível acessar a instância do banco de dados usando ferramentas como SQL Server Management Studio e Azure Data Studio.
