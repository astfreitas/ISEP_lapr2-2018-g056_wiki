# UC11 - Decidir Sobre Periodo Proposto Para Realização de Serviços

## Racional

| Fluxo Principal                                                                                        | Questão: Que Classe...                                      | Resposta                                       | Justificação                                                                                                         |
|:-------------------------------------------------------------------------------------------------------|:------------------------------------------------------------|:-----------------------------------------------|:---------------------------------------------------------------------------------------------------------------------|
|1. O Cliente inicia caso de uso |... interage com o utilizador?|DecidirSobrePeriodoUI|Pure Fabrication|
||...coordena o UC?|DecidirSobrePeriodoController|Controller|
|2. O sistema apresenta os serviços e horários atribuidos e solicita confirmação.|... conhece os serviços e horarios atribuidos? | AtribuicaoDeServicos | IE: AtribuicaoDeServicos mantém referencia ao serviço, horario e prestador atribuidos|
||...quem conhece as instancias de AtribuicaoDeServicos?|RegistoAtribucoesDePedidos| IE |
||...quem conhece a classe RegistoAtribuicoesDePedidos?|Empresa| HC + LC |
|3a. O cliente recusa a atribuição| ... guarda a decisão do cliente?|RegistoAtribucoesDePedidos| IE: por possuir as AtribuicaoDeServicos, remove a atribuição apresenta ao cliente da sua lista de atribuições|
|3b. O cliente aceita a atribuição|... guarda a decisão do cliente?|OrdemDeServico| IE: instancia criada em virtude da aceitação da atribuição. Contém as informações da atribuição.|
||...cria/instancia OrdemDeServico?|RegistoOrdemDeServicos| Creator (HC+LC)|
||...quem conhece a classe RegistoOrdemDeServicos?|Empresa| HC + LC |
|5. O sistema avisa o cliente do sucesso da operação.| | ||
                                        
## Sistematização ##

 Do racional resulta que as classes conceptuais promovidas a classes de software são:

 * Empresa
 * OrdemDeServico
 * AtribuicaoDeServicos

Outras classes de software (i.e. Pure Fabrication) identificadas:  

 * DecidirSobrePeriodoController
 * DecidirSobrePeriodoUI
 * RegistoOrdemDeServicos
 * RegistoAtribuicoesDePedidos

##	Diagrama de Sequência

![SD_UC9_IT3.png](SD_UC9_IT3.png)


##	Diagrama de Classes

![CD_UC9_IT3.png](CD_UC9_IT3.png)
