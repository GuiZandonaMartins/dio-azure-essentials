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

---Links Úteis---

Calculadora- https://azure.microsoft.com/pt-br/pricing/calculator/

Verificação de Status- https://azure.status.microsoft/pt-br/status

Curso gratuito da Microsoft- https://learn.microsoft.com/pt-br/credentials/certifications/azure-fundamentals/?practice-assessment-type=certification
