## Governança

- Azure Policy: Ajuda a impor padrões organizacionais, bloqueando a criação de certos recursos ou criando um padrão para a criação do mesmo garantindo a conformidade do ambiente. Após a policy criada, todos os usuários que utilizam a categoria selecionada estão sujeitos a esta regra. Após a criação esta policy pode estar nos seguintes estados:

	- Não Conforme:  Ficará neste estado, caso crie uma policy após a criação de recursos que estão em descordo com a mesma, esta regra será imposta para os novos recursos criados, porém não irá alterar os antigos.

	- Remediação: Possibilita a alteração de alguns recursos antigos para atenderem a regra enquanto impõe a regra para os novos recursos criados.

	-Conforme: Informa que todos os itens que atendem a esta policy estão seguindo o padrão definido.

- Bloqueio de recursos: Faz a proteção dos recursos da Azure, bloqueando a exclusão ou a alteração de um recurso, de um grupo de recursos ou de uma assinatura. Este bloqueio é herdável, ou seja, ao aplicar o bloqueio em uma assinatura, todos os grupos e recursos abaixo dela também terão este bloqueio. Existem dois tipos de bloqueio:

	- Excluir: Permite a Leitura e modificação dos dados, mas não permite excluir

	-ReadOnly: Permite somente a leitura, bloqueando qualquer alteração ou exclusão.  

	- Nota: Ao mover um recurso o bloqueio **NÃO** é herdado.

## Portal de confiança do Azure

A Azure possui um site com a documentação de compliance de cada serviço, que poderá ser consultado para obter detalhes para auditoria. Site: https://learn.microsoft.com/pt-br/azure/compliance/
 
## Microsoft Purview

É uma família de soluções de governança, risco e conformidade, avaliando estratégias de compliance, ajudando a reunir informações dos usuários que possuem acesso a certos recursos e reunindo outros tipos de dados das aplicações, sejam eles locais, multinuvem e de software como serviço.

Ele possibilita a descoberta de dados automatizada, classificação de dados confidenciais e linhagem de dados de ponta a ponto, inclusive rastrear se necessário.

## Links Úteis

- Calculadora: https://azure.microsoft.com/pt-br/pricing/calculator/

- Calculadora TCO: https://azure.microsoft.com/pt-br/pricing/tco/calculator/

- Verificação de Status: https://azure.status.microsoft/pt-br/status

- Curso gratuito da Microsoft: https://learn.microsoft.com/pt-br/credentials/certifications/azure-fundamentals/?practice-assessment-type=certification
