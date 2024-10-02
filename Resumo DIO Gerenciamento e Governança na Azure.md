## Gerenciamento de custo

Através da Azure é possível gerar relatórios de custo para identificar o custo gerado por cada recurso utilizado, também é possível criar alertas caso um recurso gere um custo maior do que o configurado ou caso exceda o orçamento definido, nesta ferramenta também é possível obter recomendações para redução de custos.

O custo final dos serviços utilizados na nuvem estão relacionados com alguns fatores são eles:

- Tipo de recurso: Cada recurso da Azure tem um custo, este custo está relacionado as funcionalidades que este recurso possui. Mesmo em recursos da mesma família, as categorias deste recurso podem afetar o custo final.

- Consumo: Com o modelo de pague pelo uso, o custo deste recurso este relacionado com o tempo em que este recurso está em utilização. Também existe o modelo de reserva, neste modelo é determinado um período de tempo que este recurso será utilizado, gerando um desconto na contratação.

- Manutenção: Monitorar o volume de utilização e adaptar a oferta dos recursos a demanda utilizada pode ajudar a reduzir os custos. 

- Área Geográfica: A localização geográfica dos recursos afeta o valor final.

- Tráfego de rede: Algumas transferências de dados de entrada são gratuitas, porém o custo para saída de dados ou transferência entre regiões Azure é afetado por zonas de cobrança.

- Assinatura: Dependendo do tipo e configuração pode alterar o custo de determinados recursos.

## Marcas/Tags

As marcas ajudam a organizar e identificar os recursos, facilitando a identificação ao pagar a fatura, **a inclusão das marcas não é obrigatória e não é um recuso herdado**, ou seja não é passada para os recursos de um grupo de recursos.

É possível criar políticas para que a inclusão da marca seja obrigatória ou para que, caso não seja informado, seja definida a marca do grupo de recursos ou ainda uma identificação aleatória seja criada. 

## Azure Marketplace

No Marketplace é possível ter acesso a aplicações virtualizadas de diversos provedores. 

Caso de algum problema nesta aplicação **não nativa do Azure**, o suporte deverá ser prestado **pelo provedor desta aplicação**.

## Calculadora de preços

Com a calculadora, é possível estimar o custo de novos recursos que serão implantados na sua conta.

Uma outra ferramenta é a calculadora de custo total (TCO), ela ajuda a estimar a economia que poderá ter ao migrar para a Azure, com relatórios comparando o custos locais com os custos de produtos da Azure na nuvem.

## Governança

- Azure Policy: Ajuda a impor padrões organizacionais, bloqueando a criação de certos recursos ou criando um padrão para a criação do mesmo garantindo a conformidade do ambiente. Após a policy criada, todos os usuários que utilizam a categoria selecionada estão sujeitos a esta regra. Após a criação esta policy pode estar nos seguintes estados:

	- Não Conforme:  Ficará neste estado, caso crie uma policy após a criação de recursos que estão em descordo com a mesma, esta regra será imposta para os novos recursos criados, porém não irá alterar os antigos.

	- Remediação: Possibilita a alteração de alguns recursos antigos para atenderem a regra enquanto impõe a regra para os novos recursos criados.

	- Conforme: Informa que todos os itens que atendem a esta policy estão seguindo o padrão definido.

- Bloqueio de recursos: Faz a proteção dos recursos da Azure, bloqueando a exclusão ou a alteração de um recurso, de um grupo de recursos ou de uma assinatura. Este bloqueio é herdável, ou seja, ao aplicar o bloqueio em uma assinatura, todos os grupos e recursos abaixo dela também terão este bloqueio. Existem dois tipos de bloqueio:

	- Excluir: Permite a Leitura e modificação dos dados, mas não permite excluir

	- ReadOnly: Permite somente a leitura, bloqueando qualquer alteração ou exclusão.  

	- Nota: Ao mover um recurso o bloqueio **NÃO** é herdado.

## Portal de confiança do Azure

A Azure possui um site com a documentação de compliance de cada serviço, que poderá ser consultado para obter detalhes para auditoria. [Site](https://servicetrust.microsoft.com/)
 
## Microsoft Purview

É uma família de soluções de governança, risco e conformidade, avaliando estratégias de compliance, ajudando a reunir informações dos usuários que possuem acesso a certos recursos e reunindo outros tipos de dados das aplicações, sejam eles locais, multinuvem e de software como serviço.

Ele possibilita a descoberta de dados automatizada, classificação de dados confidenciais e linhagem de dados de ponta a ponto, inclusive rastrear se necessário.

## Ferramentas de gerenciamento e implantação 

A Azure oferece algumas opção de ferramentas para implantar os recursos no ambiente, são elas:

- Portal da Azure: O portal padrão da Azure com uma interface gráfica para fazer todo o gerenciamento do seu ambiente.

- Azure Cloud Shell: Uma interface via linha de comando disponível dentro do portal da Azure que permite fazer a criação dos recursos utilizando apenas comandos. Possui a opção de utilizar o PowerShell ou o CLI, com a implantação via código é possível fazer a configurações do ambiente em massa rapidamente.

- ARM (Azure Resource Manager): É uma camada de gerenciamento que recebe as requisições e faz a administrações dos recursos, criando ou alterando o que foi solicitado. Os modelos do ARM são no formato JSON (Java) e podem ser utilizados para criar e implantar a infraestrutura sem precisar criar um novo código.

- Bicep: É uma linguagem de programação criada pela Microsoft, sendo compatível somente com a nuvem da mesma.

## Azure Arc

É utilizado para fazer o gerenciamento de recursos fora da nuvem da Azure, seja no ambiente local ou em outros provedores (AWS, GCP).

Também permite gerenciar recursos do Azure, fora do Azure.

Possui um painel único para o gerenciamento, utilizando todas as práticas nativas da nuvem e com um controle de acesso baseado em função, garantindo a segurança e confiabilidade.

## Ferramentas de Monitoramento

- Assistente do Azure: Analisa os recursos implantados e faz recomendações para otimizar a implantação. Ele analisa aspectos relacionados  a Confiabilidade, Segurança, Desempenho, Custo e Excelência profissional, e reúne as informações em um único local para que possamos analisa-las e, se necessário, fazermos as correções.

- Integridade do Serviço: É uma coleção de ferramentas que informam sobre o status geral do Azure, de serviços que possam afetar seu ambiente ou o status de um recurso especifico que está afetando seu ambiente, estas ferramentas são;

	- Status do Azure: Da uma visão global dos serviços da Azure.

	- Integridade do serviço: Faz a exibição apenas de serviços e regiões que estão sendo utilizados em seu ambiente.

	- Resource Health: Fornece informações sobre a integridade de seus recursos de nuvem individual.

- Azure Monitor: Maximiza a disponibilidade e o desempenho dos seus aplicativos e serviços, analisando e tomando decisões com base na telemetria da nuvem. 

## Links Úteis

- Calculadora: https://azure.microsoft.com/pt-br/pricing/calculator/

- Calculadora TCO: https://azure.microsoft.com/pt-br/pricing/tco/calculator/

- Verificação de Status: https://azure.status.microsoft/pt-br/status

- Curso gratuito da Microsoft: https://learn.microsoft.com/pt-br/credentials/certifications/azure-fundamentals/?practice-assessment-type=certification
