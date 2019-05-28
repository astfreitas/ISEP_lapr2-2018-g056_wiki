# Especificação suplementar

## Funcionalidades

-  **Segurança:**
    * As interações dos utilizadores (i.e. Cliente, Prestador de Serviços, Administrativo, Funcionário Recurso Humanos) devem ser precedidas de um processo de autenticação.
    * Excepcionalmente algumas funcionalidades bem definidas estão acessíveis sem autenticação ("A utilização da aplicação por outras pessoas está restrita ...").
    * Toda a informação da aplicação terá que ser armazenada de forma segura.
- Notificação dos Utilizadores por email consoante necessidade.

## Usabilidade

* A interação entre os diversos utilizadores e o sistema terá que ser simples, intuitiva e completamente adaptada à ação em causa.
* Dada a previsível diversidade cultural e geográfica dos vários utilizadores do sistema, este deve suportar nativamente, entre outras coisas, múltiplos fusos horários e idiomas.
* Sempre que solicitado pelos utilizadores, a aplicação deve providenciar uma ajuda/explicação devidamente contextualizada para a tarefa que o utilizador está a executar no momento.
* Considerando os diversos intervenientes no sistema e a diversidade das suas características é fundamental que a interação entre os utilizadores e o sistema seja simples, intuitiva e completamente adaptada à ação em causa.

## Fiabilidade/Confiabilidade

* No desenvolvimento do software deve-se ter em consideração que o mesmo deve ter uma taxa de disponibilidade muito elevada.
* O rastreio da informação gerada e manipulada deve ser garantido.
* Exige-se que o sistema tenha uma taxa mínima de testes de
cobertura e mutação (e.g. unitários, funcionais e de integração) de 95%.

## Desempenho

* O sistema deve estar preparado para que o tempo de resposta seja sensivelmente o mesmo independentemente da carga existente.

## Suportabilidade

* A informação da empresa (e.g. designação e NIF) deve ser especificada por configuração.
* O sistema deve também ser acessível através das mais variadas plataformas (e.g. PC, laptop, tablet, Windows, macOS), devendo a sua interface adaptar-se às características dessa plataforma.

### Restrições de design

* Adotar boas práticas de identificação de requisitos e de análise e design de software OO.
* Adoção de boas práticas de design, nomeadamente padrões GRASP.
* Reutilizar o componente de gestão de utilizadores existente na empresa.
* Adoção do processo de desenvolvimento iterativo e incremental.


### Restrições de implementação

* Com o intuito de potenciar a interoperabilidade com outros sistema já existentes e/ou em desenvolvimento, o núcleo principal do software deve ser desenvolvido em Java.
* O núcleo principal do software em Java.
* Adotar normas de codificação reconhecidas.

### Restrições de interface

--

### Restrições físicas

--
