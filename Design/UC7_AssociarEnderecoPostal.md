Realização de UC7 Associar Endereço Postal a Cliente
==========================================

Racional
--------

| Fluxo Principal                                                               | Questão: Que Classe...                             | Resposta                         | Justificação                                                                                            |
|-------------------------------------------------------------------------------|----------------------------------------------------|----------------------------------|---------------------------------------------------------------------------------------------------------|
| 1. O cliente inicia a associação de um novo endereço postal à sua informação.                     | ... interage com o utilizador?                     | AssociarEnderecoPostalUI         | PureFabrication, pois não se justifica atribuir esta responsabilidade a nenhuma classe existente no MD. |
|                                                                               | ...coordena o UC?                                  | AssociarEnderecoPostalController | Controller                                                                                              |
| 2. O sistema solicita os dados necessários (i.e. endereço postal).            | n/a                                                |                                  |                                                                                                         |
| 3. O Cliente introduz os dados solicitados.                                   | ... cria/ instancia enderecos postais?             | Cliente                          | Creator (regra 4)                                                                                       |
|                                                                               | ... guarda os dados introduzidos?                  | EnderecoPostal                   | IE - instância criada no passo 1                                                                        |
|||CodigoPostal|IE. um Endereço Postal tem um CodigoPostal|
| 4. O sistema valida e apresenta os dados, pedindo que os confirme.            | ...valida os dados do Endereço (validação local)?  | EnderecoPostal                   | IE: EnderecoPostal possui os seus próprios dados                                                        |
|                                                                               | ...valida os dados do Endereço (validação global)? | Cliente                          | IE: Cliente contém/agrega todos os seus endereços postais.                                                           |
| 5. O Cliente confirma.                                                        |                                                    |                                  |                                                                                                         |
| 6. O sistema **associa o endereço postal ao cliente** e informa-o do sucesso da operação. | ...guarda o Endereço Postal criado?                       | Cliente                   | IE: Cliente contém/agrega todos os seus endereços postais.                                      |
|                                                                               | ... notifica o utilizador?                         | AssociarEnderecoPostalUI         |                                                                                                         |



Sistematização
--------------

Do racional resulta que as classes conceptuais promovidas a classes de software
são:

- Empresa

- Cliente

- EnderecoPostal

- CodigoPostal

Outras classes de software (i.e. Pure Fabrication) identificadas:

-   AssociarEnderecoPostalUI

-   AssociarEnderecoPostalController

Diagrama de Sequência
---------------------

![SD_UC7_IT2.png](SD_UC7_IT2.png)

**Nota:** Não se considerou relevante promover (por aplicação de HC+LC) a lista de Endereços Postais de um  Cliente a uma classe especifica de software. Contudo, tal poderia ter sido feito e seria perfeitamente válido.

Diagrama de Classes
-------------------

![CD_UC7_IT2.png](CD_UC7_IT2.png)
