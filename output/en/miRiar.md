# Modelo de Informação - Guia de Implementação do Sumário de Alta (SA) da RNDS v1.0.0-release

## Modelo de Informação

### Objetivo

O documento clínico **RIA-R** (Registro de Imunobiológico Administrado em Rotina), destina-se ao registro das doses das vacinas previstas no Calendário Nacional de Imunização em atividades de vacinação rotineiras, bem como das doses aplicadas durante os estudos clínicos que subsidiaram a autorização de uso emergencial ou aprovação de registro sanitário de vacinas Covid-19 e de outras vacinas pela [Agência Nacional de Vigilância Sanitária (ANVISA)](https://www.gov.br/anvisa/pt-br).

**⚠️ ATENÇÃO:**O
**Registro de Imunobiológico Administrado em Campanha (RIA-C)**foi descontinuado. O modelo vigente é o
**Registro de Imunobiológico Administrado em Rotina (RIA-R)**

### Marcos Legais

*  [PORTARIA CONJUNTA SAES/SVSA/SEIDIGI Nº 25, DE 27 DE NOVEMBRO DE 2023](https://www.in.gov.br/web/dou/-/portaria-conjunta-saes/svsa/seidigi-n-25-de-27-de-novembro-de-2023-527017519) 

### Modelo de Informação

 O modelo de informação é uma representação conceitual e canônica, onde os elementos referentes a um documento específico são modelados em seções e blocos de dados, com seus respectivos tipos de dados a serem informados. Também são apresentadas as referências para o uso de recursos terminológicos, da seguinte maneira: 

*  **Coluna 1** - Nível: apresenta o nível do elemento no modelo de informação; 
* **Coluna 2** - Ocorrência: descreve o número de vezes (cardinalidade) que o elemento deve/pode aparecer:
*  **Coluna 3** - Seção/Item: nome do bloco ou da informação a ser enviada; 
*  **Coluna 4** - Tipo de dado: descreve o tipo de dado a ser preenchido; 
*  **Coluna 5** - Conceito: apresenta as definições do elemento; 
*  **Coluna 6** - Definição de uso do elemento: Observações e regras de negócio relacionadas ao elemento; 
*  **Coluna 7** - Conteúdo: apresenta, quando necessário, o grupo de códigos (*ValueSet*) a ser utilizado para preenchimento do elemento; 
*  **Coluna 8** - Recurso FHIR: relaciona o atributo do Modelo Informacional com o perfil do Modelo Computacional em FHIR. 

### Blocos do Modelo de Informação

 Segue abaixo o modelo de informação para o Registro de Imunobiológico Administrado em Rotina (RIA-R): 

#### Identificação do Indivíduo

| | | | | | | | |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| 1 | 1..1 | Identificação do paciente | Seção | Bloco de informações do indivíduo imunizado |  |  |  |
| 2 | 1..1 | Identificador Nacional do Indivíduo | Caracteres numéricos | Identificação unívoca dos usuários das ações e serviços de saúde, mediante número único válido em todo o território nacional. | Poderão ser utilizados para essa identificação o Cartão Nacional de Saúde (CNS) válido ou Cadastro de Pessoa Física (CPF). |  | [Registro de Imunobiológico Administrado em Rotina](StructureDefinition-BRRegistroImunobiologicoAdministradoRotina-2.0.md)*(Composition)*,[Imunobiológico Administrado em Rotina](StructureDefinition-BRImunobiologicoAdministrado-3.0.md)*(Immunization)*e[CID10 Avaliado](StructureDefinition-BRCID10Avaliado-1.0.md)*(Condition)* |
| 2 | 1..1 | Condição Maternal | Texto codificado | Identifica a condição maternal do indivíduo no ato da imunização. | Para registro da condição maternal, deverão ser utilizados os códigos disponibilizados no CodeSystem “BRCondicaoMaternal” da RNDS. | [Condição Maternal](ValueSet-BRCondicaoMaternal-1.0.md) | [Imunobiológico Administrado em Rotina](StructureDefinition-BRImunobiologicoAdministrado-3.0.md)*(Immunization)* |

#### Informações do Contato Assistencial

| | | | | | | | |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| 1 | 1..1 | Informações do Contato Assistencial | Seção | Bloco de informações do contato assistencial |  |  |  |
| 2 | 1..1 | Estabelecimento de Saúde | Caracteres numéricos | Identificação única do estabelecimento de saúde, por meio do Cadastro Nacional de Estabelecimentos de Saúde (CNES). | Código CNES do Estabelecimento de Saúde. |  | [Registro de Imunobiológico Administrado em Rotina](StructureDefinition-BRRegistroImunobiologicoAdministradoRotina-2.0.md)*(Composition)* |
| 2 | 1..1 | Identificador do profissional | Caracteres numéricos | Identifica o número do Cadastro Nacional de Saúde (CNS) do profissional de saúde que realizou o atendimento ou transcrição. | Deverá ser utilizado para a identificação, o Cartão Nacional de Saúde (CNS) do profissional. |  | [Imunobiológico Administrado em Rotina](StructureDefinition-BRImunobiologicoAdministrado-3.0.md)*(Immunization)* |

#### Registro de imunização

| | | | | | | | |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| 1 | 1..N | Registro de imunização | Seção |  |  |  |  |
| 3 | 1..1 | Grupo de Atendimento | Texto codificado | Identifica a classificação do grupo de atendimento dos indivíduos para a vacinação. | Para registro do grupo de atendimento, deverão ser utilizados os códigos disponibilizados no CodeSystem “BRGrupoAtendimento” da RNDS. | [Tipo de Grupo de Atendimento](ValueSet-BRGrupoAtendimento-1.0.md) | [Imunobiológico Administrado em Rotina](StructureDefinition-BRImunobiologicoAdministrado-3.0.md)*(Immunization)* |
| 2 | 1..1 | Estratégia de vacinação | Texto codificado | Identifica a estratégia de vacinação adotada, conforme estabelecidos pelo Programa Nacional de Imunização (PNI) e disponibilizado em CodeSystem da Rede Nacional de Dados em Saúde (RNDS). | Para registro da estratégia, deverão ser utilizado os códigos disponibilizados no CodeSystem "BREstrategiaVacinacao" da RNDS. | [Estratégia de Vacinação](ValueSet-BREstrategiaVacinacao-1.0.md) | [Imunobiológico Administrado em Rotina](StructureDefinition-BRImunobiologicoAdministrado-3.0.md)*(Immunization)* |
| 3 | 0..1 | Especialidade do profissional prescritor | Texto codificado | Identifica a especialidade do profissional que prescreveu a administração do imunobiológico por meio do Código Brasileiro de Ocupações (CBO)**Regra negocial**: Quando a estratégia de vacinação for "Especial", o campo deve ser obrigatório. | Para registro da especialidade do profissional prescritor, deverão ser utilizados os códigos da Classificação Brasileira de Ocupações (CBO) disponibilizados no CodeSystem "BRCBO" da RNDS. | [Classificação Brasileira de Ocupações (CBO)](ValueSet-BROcupacao-1.0.md) | [Imunobiológico Administrado em Rotina](StructureDefinition-BRImunobiologicoAdministrado-3.0.md)*(Immunization)* |
| 3 | 0..1 | Motivo de Indicação | Texto codificado | Identifica o código da Classificação Internacional de Doenças (CID) do motivo da indicação para administração do imunobiológico.**Regra negocial**: Quando a estratégia de vacinação for "Especial", o campo deve ser obrigatório. | Para registro do motivo da indicação para a administração do imunobiológico, deverão ser utilizados os códigos da Classificação Internacional de Doenças (CID) disponibilizados no CodeSystem "BRCID10" da RNDS. | [Classificação Internacional de Doenças - Décima Revisão (CID-10)](ValueSet-BRCID10-1.0.md) | [CID10 Avaliado](StructureDefinition-BRCID10Avaliado-1.0.md)*(Condition)* |
| 2 | 0..1 | Contato Hanseníase | Booleano | Identifica indivíduos com contato próximo de pacientes que vivem com Hanseníase.**Regra negocial**: O campo deve ser obrigatório quando o imunobiológico for vacina Bacilo Calmette - Guérim (BCG). Code 15 | Para registro do campo Contato Hanseníase, deverão ser utilizados as opções true ou false (Verdadeiro ou Falso). |  | [Imunobiológico Administrado em Rotina](StructureDefinition-BRImunobiologicoAdministrado-3.0.md)*(Immunization)* |
| 3 | 0..1 | Pesquisa Clínica | Seção | Dados do Estudo Clínico para o desenvolvimento do imunobiológico administrado |  |  | [Imunobiológico Administrado em Rotina](StructureDefinition-BRImunobiologicoAdministrado-3.0.md)*(Immunization)* |
| 4 | 0..1 | ANVISA Protocolo Estudo | Texto livre | Identifica o número do protocolo do estudo clínico autorizado pela Agência Nacional de Vigilância Sanitária para administração de vacinas. | Número do protocolo do estudo clínico na ANVISA. |  | [Imunobiológico Administrado em Rotina](StructureDefinition-BRImunobiologicoAdministrado-3.0.md)*(Immunization)* |
| 4 | 0..1 | ANVISA Protocolo Versão | Texto livre | Identifica o número da versão do protocolo do estudo clínico autorizado pela Agência Nacional de Vigilância Sanitária para administração de vacinas. | Número da versão do protocolo do estudo na ANVISA. |  | [Imunobiológico Administrado em Rotina](StructureDefinition-BRImunobiologicoAdministrado-3.0.md)*(Immunization)* |
| 4 | 0..1 | ANVISA Num Registro | Texto livre | Identifica o número do registro sanitário da vacina registrado na Agência Nacional de Vigilância Sanitária | Número do registro sanitário da vacina na ANVISA. Este registro pode ser emergencial ou definitivo. |  | [Imunobiológico Administrado em Rotina](StructureDefinition-BRImunobiologicoAdministrado-3.0.md)*(Immunization)* |
| 2 | 1..1 | Data da administração do imunobiológico | Data | Data em que o imunobiológico foi administrado. O padrão da data deve seguir a ISO8601.**Regra negocial**: A data não pode ser maior que o dia vigente. | Data em que o imunobiológico foi administrado. |  | [Imunobiológico Administrado em Rotina](StructureDefinition-BRImunobiologicoAdministrado-3.0.md)*(Immunization)* |
| 2 | 1..1 | Data e hora do registro no sistema de origem | Data | Data e hora em que o registro da vacinação foi registrado no sistema de origem. O padrão da data deve seguir a ISO8601. | Data e hora em que o registro do imunobiológico administrado foi administrado no sistema de origem. |  | [Registro de Imunobiológico Administrado em Rotina](StructureDefinition-BRRegistroImunobiologicoAdministradoRotina-2.0.md)*(Composition)* |
| 2 | 1..1 | Imunobiológico | Texto codificado | Identifica o nome do imunobiológico administrado no indivíduo. | Para registro do imunobiológico administrado, deverão ser utilizados os códigos disponibilizados no CodeSystem “BRImunobiologico” da RNDS. | [Imunobiológico](ValueSet-BRImunobiologico-1.0.md) | [Imunobiológico Administrado em Rotina](StructureDefinition-BRImunobiologicoAdministrado-3.0.md)*(Immunization)* |
| 3 | 1..1 | Fabricante | Texto codificado | Identifica o laboratório fabricante do imunobiológico administrado no indivíduo.**Regra negocial**: Para registro de transcrição de caderneta de vacinação, este campo é opcional. | Para registro do fabricante, deverão ser utilizados os códigos disponibilizados no CodeSystem “BRFabricantePNI” da RNDS. | [Fabricante do Imunobiológico](ValueSet-BRFabricanteImunobiologico-1.0.md) | [Imunobiológico Administrado em Rotina](StructureDefinition-BRImunobiologicoAdministrado-3.0.md)*(Immunization)* |
| 3 | 1..1 | Lote | Texto livre | Identifica o lote do imunobiológico de acordo com o fabricante.**Regra negocial**: Para registro de transcrição de caderneta de vacinação, este campo é opcional. | O lote é fundamental para identificação de características do imunobiológico. É uma informação presente na embalagem do produto ou, algumas vezes, na caderneta de vacinação. |  | [Imunobiológico Administrado em Rotina](StructureDefinition-BRImunobiologicoAdministrado-3.0.md)*(Immunization)* |
| 2 | 1..1 | Dose | Texto codificado | Identifica o registro da dose da vacina administrada no indivíduo. | Para registro da dose da vacina administrada, deverão ser utilizados os códigos disponibilizados no CodeSystem “BRDose” da RNDS. | [Dose do Imunobiológico](ValueSet-BRDose-1.0.md) | [Imunobiológico Administrado em Rotina](StructureDefinition-BRImunobiologicoAdministrado-3.0.md)*(Immunization)* |
| 2 | 1..1 | Via de administração | Texto codificado | Identifica a via com que o imunobiológico administrado entra em contato com o organismo. | Para registro da via de administração, deverão ser utilizados os códigos disponibilizados no CodeSystem "BRViaAdministracao" da RNDS. | [Via de Administração do Imunobiológico](ValueSet-BRViaAdministracao-1.0.md) | [Imunobiológico Administrado em Rotina](StructureDefinition-BRImunobiologicoAdministrado-3.0.md)*(Immunization)* |
| 2 | 1..1 | Local de aplicação | Texto codificado | Identifica a localização anatômica em que o imunobiológico foi aplicado. | Para registro do local de administração da vacina, deverão ser utilizados os códigos disponibilizados no CodeSystem "BRLocalAplicacao" da RNDS. | [Local de Aplicação](ValueSet-BRLocalAplicacao-1.0.md) | [Imunobiológico Administrado em Rotina](StructureDefinition-BRImunobiologicoAdministrado-3.0.md)*(Immunization)* |
| 2 | 1..1 | Transcrição de Caderneta | Booleano | Identifica se o registro de vacinação é uma transcrição de caderneta | Para a identificação de que o registro se trata de uma transcrição, deverá ser utilizado o código apropriado presente no CodeSystem "BRRegistroOrigem" na RNDS. | [Registro de Origem](ValueSet-BRRegistroOrigem.md) | [Imunobiológico Administrado em Rotina](StructureDefinition-BRImunobiologicoAdministrado-3.0.md)*(Immunization)* |
| 3 | 0..1 | Indicação do país de origem do registro da vacina. | Texto codificado | Identifica se o registro da administração da vacina, realizado por transcrição de caderneta, foi realizado no Brasil ou em outro País. | Para a identificação de qual país o registro de imunização transcrito foi realizado, deverão ser utilizados os códigos disponibilizados no CodeSystem "BRPais" da RNDS. | [País](ValueSet-BRPais-1.0.md) | [Imunobiológico Administrado em Rotina](StructureDefinition-BRImunobiologicoAdministrado-3.0.md)*(Immunization)* |

