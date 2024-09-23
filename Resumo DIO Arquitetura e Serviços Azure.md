## Organização

- Conta: A conta principal do cliente.

- Grupos de gerenciamento: Faz o gerenciamento de uma ou mais assinaturas, podemos também definir regras que serão distribuídas para as assinaturas que estão abaixo do grupo.

- Assinatura: Dentro de uma **conta** do Azure é possível ter várias **assinaturas** diferentes (já as assinaturas estão **limitadas** a apenas uma **conta/dono**). É gerada uma fatura para cada assinatura, facilitando a organização no hora de pagar. É possível definir quais os recursos que cada assinatura terá acesso.

- Grupo de recursos: Um grupo de recursos organiza os recursos criados dentro dele, facilitando a localização ou exclusão deles. 

## Serviços de Computação

A computação do Azure é um serviço sob demanda que fornece recursos de computação.

- Máquinas Virtuais: Uma máquina armazenado na nuvem, o cliente tem acesso a toda a configuração do software enquanto o provedor cuida da parte do hardware que será utilizado. O cliente não tem nenhum acesso ao hardware da máquina e, até o momento, nem mesmo a Bios.

	- lift-and-shift: É uma forma de migração da sua máquina na estado que está atualmente.

- Conjunto de **dimensionamento** de VMs: Traz um conjunto de VMs idênticas com a oportunidade de balancear a carga entre elas para dimensionar os recursos automaticamente.

- Conjuntos de **disponibilidade**: Um conjunto de VMs separadas em dois grupos: 

 	- Domínio de falha: Máquinas separadas em racks diferentes dentro do datacenter, em caso de falha ou manutenção em um rack o outro grupo assume a carga.

	- Domínio de atualização: Separa a máquinas de diferentes racks em grupos para evitar que todas atualizem ao mesmo tempo. Enquanto um grupo atualiza o outro assume a carga, somente após o termino das atualizações do primeiro grupo, o segundo inicia o processo. 

- Área de trabalho virtual do Azure: É uma virtualização da sua área de trabalho, ao invés da empresa disponibilizar um computador, o funcionário utiliza e seu próprio e acessa a área da empresa de forma remota.

- Contêineres do Azure: Fornece um ambiente leve e virtualizado que não exige o gerenciamento de um Sistema Operacional e proporciona uma rápida escalabilidade. Ofertando sempre serviços **PaaS**.

	- Instâncias de Contêiner: Executa um contêiner ou um pod de contêineres no Azure.

	- Aplicativos de Contêiner: Não exige que se faça um gerenciamento de contêineres. Possibilita o balanceamento de carga e colocação em escala, permitindo maior flexibilidade no design.

	- Serviços de Kubernetes do Azure (AKS): Um serviço de orquestração dos contêineres. Permitindo o gerenciamento do tempo de vida dos contêineres.

- Azure Functions: Uma oferta Paas. Trabalha com o modelo de funções onde não é necessário possui um servidor para executa-la, somente uma situação (gatilho) em que esta função será disparada.

## Serviços de Aplicativos

- Possibilita a criação de aplicativos e dimensionamento web e de APIs, é compatível com Windows e Linux e permite implantações automatizadas. É uma excelente opção de hospedagem do seu aplicativo, perimindo hospedar a versão de produção do seu aplicativo e também versões que estão em desenvolvimento.

- Trabalha com as linguagens .NET, .NET Core, Node.js, Java, Pyton ou php. 

- **É uma oferta Paas.**

## Serviços de rede

- Rede virtual da Azure (VNet): Permite a comunicação dos recursos dentro do Azure. Duas VNets não se comunicam por padrão, mas é possível permitir esta comunicação via emparelhamento de rede, da mesma forma com uma rede local (on-premisse).

	- Sub-redes: As sub-redes segmentam a rede principal, criando um endereço de IP para cada recurso, mas sempre respondendo a VNet.

- Gateway de VPN: Trafega de forma criptografada os dados entre uma rede virtual da Azure e uma rede local.

- ExpressRoute: É uma comunicação direta, via cabo, entre sua empresa e os servidores da Azure.

- DNS do Azure: O DNS faz a tradução de um nome amigável e legível para humanos, para um endereço de IP para que a máquina consiga entender. Dentro da Azure é possível gerenciar este recurso de forma mais ágil, seja de ambientes externos ou do próprio Azure e permite criar nomes de domínio privados personalizados.

## Armazenamento

- Contas de Armazenamento: Um serviço que pode receber diversos tipos de dados, tem um funcionamento parecido com um grupo de recursos e precisa ter um nome exclusivo globalmente.

- Redundância de Armazenamento: É possível  configurar a replicação dos dados armazenados para garantir que os mesmos não serão perdidos ou fiquem indisponíveis, as formas de configuração são:

	- Redundância Local (LRS): Armazenamento em um único datacenter instalado na região primária escolhida, neste datacenter são cridas três cópias  que são armazenadas em discos diferentes, durabilidade de 11 noves.

	- Redundância de Zona (ZRS): Armazenado em três datacenters dentro da região primária, durabilidade de 12 noves

	- Redundância Geográfica (GRS): Usa a mesma estratégia do LRS porém em duas regiões diferentes, a região primária e o seu par, durabilidade de 16 noves.

	- Redundância de Zona Geográfica (GZRS): Armazenamento em três datacenters na região primária e, em uma região diferente, faz o armazenamento em um único datacenter, durabilidade de 16 noves.

- Blob: Otimizado para o armazenamento de quantidades massivas de dados *não estruturados* como texto ou dados binários.

- Discos: Fornece os discos (HDD ou SSD) paras as máquinas virtuais, sendo possível alocar discos adicionais após a criação da VM enquanto ela está rodando.

- Filas: Faz o armazenamento de mensagens, possibilitando uma futura recuperação desta informação.

- Arquivos: Configura um compartilhamento de rede dos das informação, sendo possível mapear na maquina do usuário o local onde os dados estão armazenados para facilitar o acesso.

- Tabelas: Fornece uma opção de chave/atributo para o armazenamento de dados *estruturados*, não relacionais com um design sem esquema.

### Ponto de extremidade público 

Este é o endereço que as aplicações citadas aplicações irão gerar para possibilitar o acesso posterior ou apontamento para uma aplicação. 

O endereço segue um padrão: **https://<nome-da-conta-da-armazenamento>.<nome-do-serviço-utilizado>.core.windows.net**

Exemplo:  https://ArmazenamentoDIO.blob.core.windows.net

### Camadas de acesso de armazenamento

Durante a criação dos serviços, é necessário indicar a camada em que o mesmo será armazenado, estas camadas são:

- Frequente: Otimizado para armazenamento de dados acessados com frequência.

- Esporádico Otimizados para dados com pouca frequência de acessos e armazenados por pelo menos 30 dias.

- Frio: Otimizados para dados com pouca frequência de acessos e armazenados por pelo menos 90 dias.

- Arquivo Morto: Otimizado para dados raramente acessados, armazenados por pelo menos 180 dias e com latência flexível.

## Migração

- Azure Data Box: É um equipamento físico que faz a cópia dos dados on-premisse e é levado até o datacenter da Microsoft para ser integrado, os dados são criptografados e transportados em uma caixa robusta que armazena até 80 terabytes de dados. Normalmente é utilizado para transferir dados de locais remotos com uma conexão limitada ou sem conexão.

- AZCopy: Faz a cópia dos dados, via linha de comando, para um blob ou arquivo na Azure. **Sincroniza os dados em apenas uma direção**.

-  Gerenciador de Armazenamento: Tem a funcionalidade do AZCopy porém com uma interface gráfica, facilitando o processo de migração. Compatível com Windows Mac e Linux. 

- Sincronização de arquivos: **Sincroniza os dados de forma Bidirecional**, os arquivos acessados com frequência são mantidos no local, enquanto os demais são migrados, liberando espaço.

## Segurança

A parte de segurança trabalha com o conceito confiança zero e de defesa em profundidade, montando várias camadas de defesa para o acesso aos dados, com o objetivo de retardar o avanço de uma possível invasão e evitar o acesso indevido as informações armazenadas.

- Autenticação x Autorização

	- Autenticação: É a confirmação de que as credenciais informadas estão corretas.

	- Autorização: Determina o nível de acesso do usuário, definindo quais recursos ou informações o usuário terá cesso.

- Microsoft Entra ID: É o serviço de gerenciamento de identidades, validando suas credenciais durante o acesso as aplicações. Ele garante a autenticação dos usuários, o logon único (SSO e o gerenciamento de aplicativos e dispositivos.

- Microsoft Entra Domain Services: Faz sincronização dos usuário do serviço de AD local para o Entra ID na Azure. Ao criar um novo usuário no AD local o mesmo é replicado para o serviço na nuvem permitindo a autenticação nos dois ambientes.

- Microsoft Entra External ID: Possibilita que usuário externos façam o acesso ao seu ambiente de forma confiável ou aplicação, através de contas confiáveis como a conta do Google.

- Autenticação Multifator: Garante uma segurança adicional, solicitando elementos adicionais para a autenticação, como digitar um código ou inserir um Smartcard.

- Acesso Condicional: Faz o monitoramento das informações do usuário durante o acesso, permitindo ou não o acesso em determinadas situações.

- Controle de acesso baseado em função: É possível gerenciar cada recurso que o usuário terá acesso, garantindo que acesso somente os recursos necessário para fazer o trabalho. A permissão de acesso a recurso é herdada para os serviços que estão abaixo dele, Exemplo: ao dar permissão de acesso ao usuário em um grupo de recursos, o mesmo terá acesso a todos os recursos que estão abaixo deste grupo.

- Microsoft Defender para a nuvem: É um serviço que monitora e fornece proteção contra ameaças nos datacenters da Azure e locais, fornece também sugestões de correções para os problemas apresentados. Este serviço possui comunicação com a AWS e GCP, conseguindo apontar problemas fora do ambiente da Microsoft.
 
## Links Úteis

Primeiro Resumo:

Calculadora: https://azure.microsoft.com/pt-br/pricing/calculator/

Verificação de Status: https://azure.status.microsoft/pt-br/status

Curso gratuito da Microsoft: https://learn.microsoft.com/pt-br/credentials/certifications/azure-fundamentals/?practice-assessment-type=certification
