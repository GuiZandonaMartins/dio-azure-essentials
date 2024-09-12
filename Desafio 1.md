# Como criar uma máquina Virtual na Azure

## 1. Acesse o portal da Azure

- Acesse [o portal da Azure](portal.azure.com) e efetue o login.
- Caso não tenha uma conta, é possível [criar uma gratuitamente](https://azure.microsoft.com/pt-br/pricing/purchase-options/azure-account?icid=azurefreeaccount).

## 2. Criando a máquina virtual

- No menu esquerdo, selecione **Máquinas Virtuais**.

- Clique em **Criar** no topo da tela.

## 3. Escolher a assinatura e o grupo de recursos

- Selecione a assinatura que deseja utilizar para criar a VM.

- Escolha um grupo de recursos existente ou crie um novo. 

    *Com o grupo de recursos é possível organizar e gerenciar os recursos relacionados*.

## 4. Defina a base da VM

- Nome da máquina virtual: Defina um nome para a sua VM.
- Região: Escolha a região onde a VM será criada. A escolha da região pode afetar o custo e a latência.
- Opção de disponibilidade: Defina se a VM ficará em uma zona ou conjunto de disponibilidade, para alta disponibilidade.
- Imagem: Selecione a imagem do sistema operacional que será utilizado na VM.
- Tamanho da VM: Defina o tamanho da VM com base nas suas necessidades de processamento (memória e armazenamento) e de custo.

## 5.Definir as credenciais de acesso

- Usuário e senha: Defina **o nome do usuário** que terá privilégios de administrador e uma **senha** que siga os critérios de senha forte.

- SSH: Ou selecione a autenticação por chave SSH (Normalmente utilizada para acesso em máquinas Linux).

  *Lembre-se de guardar essas informações, pois serão necessárias para fazer o acesso remoto na VM.*

## 6.Configuração de rede

- Rede virtual: Crie uma rede virtual ou selecione uma já existente.

- Sub-rede: Escolha ou crie uma sub-rede dentro da rede virtual.

- Grupos de segurança de rede (NSG): Configure as regras de segurança e acesso para a VM.

## 7. Gerenciamento de disco

- Disco do sistema operacional: Selecione o tipo de disco SSD ou HDD que deseja usar para a VM.

- Disco de dados: Neste momento, também é possível alocar um disco adicional a sua VM

## 8. Revisar e criar

- Revise todas as configurações e clique em **Revisar e Criar**, após a validação clique em **Criar** e aguarde o processo de criação.

## 9. Acessar a VM

#### Após a criação da VM, você poderá acessa-la por sua formas:
- Para máquina virtual **Windows**, utilize o **Remote Desktop (RDP)**.
- Para máquina virtual **Linux**, utilize o **SSH**.

#### Após a criação da máquina virtual, é possível gerencia-la através do portal Azure, fazendo alterações, alocando mais recursos e, quando não tiver mais utilidade, exclui-la para reduzir os custos. 
