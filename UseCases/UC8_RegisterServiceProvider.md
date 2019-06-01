# UC8 - Registar Prestador de Serviço

## Formato Breve

O FRH inicia o registo do novo Prestador de Serviço. O sistema solicita o NIF do prestador de serviços a registar. O FRH indica o NIF do prestador de serviços a registar. O sistema apresenta os dados do prestador de serviços (i.e. nome completo, NIF, email institucional, endereço postal, contacto telefónico, categorias de serviços) indicado e solicita confirmação. O FRH confirma os dados ou procede à sua edição. O sistema valida e apresenta os dados, pedindo que os confirme. O FRH confirma os dados apresentados pelo sistema. O sistema regista os dados do novo Prestador de Serviço e informa o FRH do sucesso da operação. O sistema envia os dados de acesso ao novo Prestador de Serviço.

## SSD
![UC8-SSD-IT4.png](SSD_UC8_IT4.png)

## Formato Completo

### Ator principal

Funcionário de Recursos Humanos (FRH)

### Partes interessadas e seus interesses
* **FRH** pretende registar os Prestadores de Serviço para que seja possível disponibilizar os serviços prestados pela empresa.
* **Empresa:** pretende que o Prestador de Serviço esteja disponível para realizar os serviços solicitados pelos seus clientes.
* **Prestador de Serviço** necessita de ter um perfil de acesso para indicar a sua disponibilidade por forma a realizar os serviços solicitados pelos clientes da Empresa.


### Pré-condições
Existirem Categorias de Serviços e Áreas Geográficas definidas no sistema.

### Pós-condições
A informação do registo é guardada no sistema.

## Cenário de sucesso principal (ou fluxo básico)

1. O FRH inicia o registo dum novo Prestador de Serviço.
2. O sistema solicita o NIF do prestador de serviços a registar.
3. O FRH introduz o NIF do prestador de serviços.
4. O sistema apresenta os dados do prestador de serviços (i.e. nome completo, NIF, email institucional, endereço postal, contacto telefónico).
5.  O sistema apresenta a hipostese de o FRH escolher confirmar os dados apresentados ou de introduzir os dados - **alternate.**
6.
		a. **O FRH não aceita os dados e inicia introdução manual dos dados.**
		6.1. O FRH introduz os dados solicitados.
		6.2. O sistema mostra as categorias de serviços existentes e solicita uma.
		6.3. O FRH seleciona a categoria de serviço pretendida.
		6.4. O sistema valida e guarda a categoria selecionada.
		6.5. Os passos 6.2 a 6.4 repetem-se enquanto não forem selecionadas todas as categorias pretendidas (mínimo 1).
		6.6. O sistema mostra as áreas geográficas existentes e solicita uma.
		6.7. O FRH seleciona a área geográfica pretendida.
		6.8. O sistema valida e guarda a área geográfica selecionada.
		6.9. Os passos 6.6 a 6.8 repetem-se enquanto não forem selecionadas todas as áreas geográficas pretendidas (mínimo 1).
		6.10. O sistema valida e apresenta os dados, pedindo que os confirme.
		6.11. O FRH confirma.
		6.12. O sistema regista os dados do novo Prestador de Serviço, envia os dados de acesso ao novo Prestador de Serviço e informa o FRH do sucesso da operação.
		**Fim de alternate 6.a**

		b. **O FRH aceita e confirma os dados fornecidos pelo sistema**
		6.1. O sistema mostra as categorias de serviços da candidatura
		6.2. O sistema apresenta hipotese de escolher confirmar as categorias apresentadas ou de escolher novamente categorias.- **alternate.**

				c. **O FRH não aceita as categorias e inicia a selecção de novas categorias**
				6.2.1. O sistema mostra as categorias de serviços existentes e solicita uma.
				6.2.2. O FRH seleciona a categoria de serviço pretendida.
				6.2.3. O sistema valida e guarda a categoria selecionada.
				6.2.4. Os passos 6.2.1 a 6.2.3 repetem-se enquanto não forem selecionadas todas as categorias pretendidas (mínimo 1).
				6.2.5. O sistema mostra as áreas geográficas existentes e solicita uma.
				6.2.6 O FRH seleciona a área geográfica pretendida.
				6.2.7 O sistema valida e guarda a área geográfica selecionada.
				6.2.8 Os passos 6.2.5 a 6.2.7 repetem-se enquanto não forem selecionadas todas as áreas geográficas pretendidas (mínimo 1).
				6.2.9. O sistema valida e apresenta os dados, pedindo que os confirme.
				6.2.10. O FRH confirma.
				6.2.11 O sistema regista os dados do novo Prestador de Serviço, envia os dados de acesso ao novo Prestador de Serviço e informa o FRH do sucesso da operação.
				**Fim de alternate 6.2.c**

				d. **O FRH aceita as categorias - prossegue para enumeração 7**
7. O sistema mostra as áreas geográficas existentes e solicita uma.
8. O FRH seleciona a área geográfica pretendida.
9. O sistema valida e guarda a área geográfica selecionada.
10. Os passos 7 a 9 repetem-se enquanto não forem selecionadas todas as áreas geográficas pretendidas (mínimo 1).
11. O sistema valida e apresenta os dados, pedindo que os confirme.
12. O FRH confirma.
13.	O sistema regista os dados do novo Prestador de Serviço, envia os dados de acesso ao novo Prestador de Serviço e informa o FRH do sucesso da operação.


### Extensões (ou fluxos alternativos)

*a. O FRH solicita o cancelamento da registo.

> O caso de uso termina.

3a. O FRH introduz um NIF não valido.
> 1. O sistema informa que o NIF não é válido e volta a solicitar NIF.
> 2. FRH submete. O caso de uso continua.


3a. dados de numero mecanográfico e/ou nome completo/abreviado e/ou email duplicados.
>	1. O sistema informa o FRH sobre a duplicação dos dados.
>	2. O sistema permite a introdução de novos dados
>
	>	2a. O FRH não altera os dados. O caso de uso termina.

6a. Dados de Categoria incompletos/duplicados.
>	1. O sistema informa quais os dados em falta ou duplicados
>	2. O sistema permite a introdução de novos dados
>
	>	2a. O FRH não altera os dados. O caso de uso termina.

10a. Dados de Área Geográfica incompletos/duplicados.
  >	1. O sistema informa quais os dados em falta ou duplicados
  >	2. O sistema permite a introdução de novos dados
  >
  	>	2a. O FRH não altera os dados. O caso de uso termina.


12a. O sistema deteta que os dados (ou algum subconjunto dos dados) introduzidos devem ser únicos e que já existem no sistema.
>	1. O sistema alerta o FRH para o facto.
>	2. O sistema permite a sua alteração
>
	>	2a. O FRH não altera os dados. O caso de uso termina.

12b. O sistema detecta que os dados introduzidos (ou algum subconjunto dos dados) são inválidos.
> 1. O sistema alerta o FRH para o facto.
> 2. O sistema permite a sua alteração.
>
	> 2a. O FRH não altera os dados. O caso de uso termina.

### Requisitos especiais
\-

### Lista de Variações de Tecnologias e Dados
\-

### Frequência de Ocorrência
\-

### Questões em aberto

* Existem outros dados obrigatórios para além dos já conhecidos?
* Quais os dados que em conjunto permitem detetar a duplicação de Prestadores de Serviço?
* Quais são as regras de segurança aplicáveis aos dados de acesso?
* Qual é o sistema de email a adotar?
* Temos que suportar mais do que um sistema de email?
* Como é definido qual é o sistema de email a usar?
* Qual a frequência de ocorrência deste caso de uso?
