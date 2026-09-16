# Modelo de Informação - Guia de Implementação do Sumário de Alta (SA) da RNDS v1.0.0-release

## Modelo de Informação

### Objetivo

O documento clínico **RIA-R** (Registro de Imunobiológico Administrado em Rotina), destina-se ao registro das doses das vacinas previstas no Calendário Nacional de Imunização em atividades de vacinação rotineiras, bem como das doses aplicadas durante os estudos clínicos que subsidiaram a autorização de uso emergencial ou aprovação de registro sanitário de vacinas Covid-19 e de outras vacinas pela [Agência Nacional de Vigilância Sanitária (ANVISA)](https://www.gov.br/anvisa/pt-br).

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

 Segue abaixo o modelo de informação para o Sumário de Alta (SA): 

