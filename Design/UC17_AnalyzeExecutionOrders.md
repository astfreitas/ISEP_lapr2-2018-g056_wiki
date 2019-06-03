# Realization of UC17 - Analyze Execution Orders

## Rational

| Flow Main                                                                                        | Question: Which class...                                      | Answer                                       | Justification                                                                                                         |
|:-------------------------------------------------------------------------------------------------------|:------------------------------------------------------------|:-----------------------------------------------|:---------------------------------------------------------------------------------------------------------------------|
|1. The Service Provider initiates the analyze execution orders.|... interacts with the user?|AnalyzeExecutionOrdersUI|Pure Fabrication|
||...coordinates the UC?|AnalyzeExecutionOrdersController|Controller|
||...knows the ExecutionOrdersRegistry?|Company|IE|
||...knows the Execution Orders?|ExecutionOrdersRegistry|HC + LC|
|2. The systems displays every execution orders and provides the choice to sort the list by the parameters available on execution orders (name, distance between SP and client's postal address, service category, service start date and time, type of service and by client's address).||||
|3. The service provider triggers the desired parameter to sort.||||
|4. The systems sorts the execution orders list by the selected parameter and displays it.||||

## Systematization ##

From the rationale results that the following conceptual classes are promoted to software classes are:





Other software classes (i.e. Pure Fabrication) identified:  




##	Detail Diagram

![SD_UC17_IT4.png](SD_UC17_IT4.png)



##	Class Diagram
- Como permitir escolha de parametros? por Lista de parametros - registo parametros?
- Lista de Ordens de Execução a mostrar e 'manipular' será por composição?
- Qual classe responsavel por aplicar sort?
