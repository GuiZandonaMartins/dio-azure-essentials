# Configurando Recursos e Dimensionamentos em Máquinas Virtuais no Azure

## 1. Acesse o portal da Azure

- Acesse o [portal da Azure](portal.azure.com) e efetue o login.

## 2. Criar uma Máquina Virtual

- No menu esquerdo, selecione Máquinas Virtuais.

- Clique em Criar no topo da tela.

- Escolha uma assinatura e um grupo de recursos existente ou crie um novo.

- Defina o nome da VM e escolha a região onde ela será hospedada.

- Tamanho da VM: Defina o tamanho da VM com base nas suas necessidades de processamento (memória e armazenamento) e de custo.

- Escolha a imagem do sistema operacional para a VM, como Windows ou Linux. 

- Defina as credenciais de login, usuário e senha para Windows ou Chave SSH para Linux.

## 6.Configuração de rede

- Rede virtual: Crie uma rede virtual ou selecione uma já existente.

- Sub-rede: Escolha ou crie uma sub-rede dentro da rede virtual.

- Grupos de segurança de rede (NSG): Configure as regras de segurança e acesso para a VM.

## 7. Gerenciamento de disco

- Disco do sistema operacional: Selecione o tipo de disco SSD ou HDD que deseja usar para a VM.

- Disco de dados: Neste momento, também é possível alocar um disco adicional a sua VM

## 8. Definir Dimensionamento Automático (Autoescala)

- Para aplicações que variam em demanda, é possível configurar a Autoescala. Isso permite que o Azure ajuste automaticamente o número de instâncias da VM com base no uso de CPU, memória ou outros critérios.

- Configure as regras de escalabilidade baseadas em métricas de desempenho da VM.

## 9. Configurar Backups e Recuperação

- Habilite backup automático na aba de Backup. Isso permitirá que você configure políticas de backup para garantir a recuperação dos dados em caso de falhas.

- Defina a retenção de backups e o agendamento de acordo com as necessidades da sua aplicação.

## 10. Configurar o Dimensionamento Manual

- Para ambientes que precisam de ajustes manuais, você pode alterar o tamanho da VM ou adicionar novos recursos manualmente após a criação.

- No menu da máquina virtual, vá até Dimensionar para alterar o tipo de instância (mais memória, CPU ou armazenamento) de acordo com as mudanças na carga de trabalho.

## 11. Monitorar e Ajustar Desempenho

- Depois que a VM estiver funcionando, é importante monitorar o uso de recursos. No painel da VM, acesse Métricas para visualizar o consumo de CPU, memória e rede.

- Utilize Alertas para receber notificações quando os limites definidos forem atingidos, permitindo ajustes rápidos e evitando gargalos.

## 12. Revisar e criar

- Revise todas as configurações e clique em **Revisar e Criar**, após a validação clique em **Criar** e aguarde o processo de criação.

## 13. Acessar a VM

#### Após a criação da VM, você poderá acessa-la por sua formas:
- Para máquina virtual **Windows**, utilize o **Remote Desktop (RDP)**.
- Para máquina virtual **Linux**, utilize o **SSH**.

## 14. Gerenciar e Dimensionar Após a Criação

- É possível ajustar os recursos da VM a qualquer momento, acessando a aba de Dimensionamento no painel de configurações, adicionando novas VMs à  rede ou usar um Balanceador de Carga para distribuir o tráfego entre as VMs
