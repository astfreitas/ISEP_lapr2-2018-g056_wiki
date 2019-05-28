# Análise OO #
O processo de construção do modelo de domínio é baseado nos casos de uso, em especial os substantivos utilizados, e na descrição do enunciado.
## Racional para identificação de classes de domínio ##
Para a identificação de classes de domínio usa-se a lista de categorias das aulas TP (sugeridas no livro). Como resultado temos a seguinte tabela de conceitos (ou classes, mas não de software) por categoria.

### _Lista de Categorias_ ###

**Transações (do negócio)**

* Pedido Prestação Serviço;
* Candidatura

---

**Linhas de transações**

* Preferência Horário
* Descrição Serviço Pedido
* Outro Custo Adicional

---

**Produtos ou serviços relacionados com transações**

*  Serviço
*  Serviço Fixo
*  Serviço Limitado
*  Serviço Expansível

---


**Registos (de transações)**

*  

---  


**Papéis das pessoas**

* Administrativo
* Funcionário Recursos Humanos (FRH)
* Cliente
* Prestador de Serviços
* Utilizador
* Utilizador Não Registado

---


**Lugares**

*  Área Geográfica
*  Endereço Postal
* Código Postal

---

**Eventos**

*

---


**Objectos físicos**

*


---


**Especificações e descrições**

*  (Especificar) Categoria (de Serviço)
*  (Especificar) Serviço
*  Habilitação Académica
*  Habilitação Profissional
* Disponibilidade
*  Tipo de Serviço
* Estado de Candidatura
* OrdemServico

---


**Catálogos**

*  

---


**Conjuntos**

*

---


**Elementos de Conjuntos**

*  

---


**Organizações**

*  Empresa

---

**Outros sistemas (externos)**

*  (Componente Gestão Utilizadores)
*  Servico Externo

---


**Registos (financeiros), de trabalho, contractos, documentos legais**

*

---


**Instrumentos financeiros**

*  

---


**Documentos referidos/para executar as tarefas/**

* Documento Comprovativo   

---



###**Racional sobre identificação de associações entre classes**###

Uma associação é uma relação entre instâncias de objectos que indica uma conexão relevante e que vale a pena recordar, ou é derivável da Lista de Associações Comuns:

+ A é fisicamente (ou logicamente) parte de B
+ A está fisicamente (ou logicamente) contido em B
+ A é uma descrição de B
+ A é conhecido/capturado/registado por B
+ A usa ou gere B
+ A está relacionado com uma transacção de B + etc.



| Conceito (A) 		|  Associação   		|  Concept (B) |
|----------	   		|:-------------:		|------:       |
| Administrativo  	| especifica     	| Categoria  |
|   					| especifica     	| Serviço  |
|   					| especifica     	| Área Geográfica  |
|   					| trabalha para     | Empresa  |
|						| atua como			| Utilizador |
| Empresa				| presta     			| Serviço  |
|						| tem     			| Categoria  |
|						| atua em    			| Área Geográfica  |
| 						| possui     			| Cliente  |
| 						| possui     			| Administrativo  |
| 						| possui     			| FRH  |
| 						| possui     			| Prestador de Serviços  |
| 						| recebe     			| Pedido de Prestação de Serviços  |
| 						| recebe     			| Candidatura a Prestador de Serviços   |
| 						|define		| Serviço Externo    |
| 						|tem (vários)	| Tipo de Serviço    |
|             |emite        | Ordem de Serviço   |
| Serviço				| catalogado em     | Categoria  |
|						| é solicitado em	| Pedido de Prestação de Serviços |
|						| referido em			| Descrição Serviço Pedido |
|						| é de (um)		| Tipo Serviço  |
| Serviço Fixo	| é uma especialização     | Serviço  |
| Serviço Limitado	| é uma especialização  | Serviço  |
| Serviço Expansível	| é uma especialização  | Serviço  |
| Cliente				| possui     			| Endereço Postal  |
|						| atua como			| Utilizador |
|						| realiza				| Pedido de Prestação de Serviços |
| Categoria			| cataloga    		| Serviço  |
|						| mencionada em     | Candidatura a Prestador de Serviços  |
|						| mencionada em     | Prestador de Serviços  |
| Prestador de Serviços| atua como		| Utilizador |
|  						| indica (várias)| Disponibilidade |
|  						| realiza serviços em (várias)| Área Geográfica |
|  						| realiza serviços catalogados em (várias)| Categoria |
| FRH					| atua como		| Utilizador |
| Candidatura a Prestador de Serviços |  menciona | Endereço Postal
| 						|  menciona 		| Habilitação Académica
| 						|  menciona 		| Habilitação Profissional
| 						|  menciona 		| Categoria de Serviço
| 						|  tem anexado 	| Documento Comprovativo
|             |  tem          | Estado de Candidatura
| Pedido de Prestação de Serviços 	| é feito por | Cliente |
| 					   | inclui 			| Outro Custo Adicional |
| 					   | indica 			| Preferência Horário |
| 					   | possui 			| Descrição Serviço Pedido |
|						| para realizar-se em| Endereço Postal |
| Descrição Serviço Pedido	 | consta	| Pedido de Prestação de Serviços |
| 								 | referente |  Serviço |
| Area Geográfica	 | centra-se em	| Codigo Postal|
|  						 | recorre a		| Serviço Externo|
|  						 | atua em (vários)| Codigo Postal|
| Serviço Externo | informa/disponibiliza|(Distância+CódigoPostal)|
| Endereço Postal	 | tem (um)		| Codigo Postal|
| Ordem de Serviço | atribuída a | Prestador de Serviço
|                  | referente a | Pedido de Prestação de Servico |


**Nota:** Os serviços externos disponibilizam a distância para códigos postais. Cada par de informação Distância+CódigoPostal é usado para estabelecer a associação "atua em" entre AreaGeografica e CódigoPostal.


## Modelo de Domínio

![MD_IT3.png](MD_IT3.png)
