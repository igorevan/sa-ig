# Modelo Computacional - Guia de Implementação do Sumário de Alta (SA) da RNDS v1.0.0-release

## Modelo Computacional

### Modelo Computacional

 Para a modelagem do modelo computacional do Sumário de Alta (SA), foram mapeados os campos do Modelo de Informação (MI) aos recursos internacionais [FHIR R4](https://hl7.org/fhir/R4/). Assim, foi realizada a modelagem fechada dos perfis de modo a atender o contexto nacional. 

Foi criado um [Projeto Rede Nacional de Dados em Saúde](https://simplifier.net/redenacionaldedadosemsaude/), na plataforma [SIMPLIFIER.NET](https://simplifier.net/), para a publicação e distribuição dos perfis relacionados aos documentos computacionais em produção na rede.

### Bundle de Envio do SA

O diagrama abaixo apresenta o pacote *Bundle* no qual é condensado o Sumário de Alta (SA), referenciando todos os dados relevantes para caracterizar o sumário.

 **Figura 1 - Diagrama do *Bundle* do SA** 

### Recursos FHIR

 O modelo computacional do SA é definido pelo perfil BRSumarioAlta [`Composition`].

Extensões utilizadas:

Perfis dos tipos *ValueSet* e *CodeSystem* estão associados a recursos terminológicos. No contexto de imunizações e os domínios utilizados, foram criados * CodeSystems* específicos definidos pelo [Comitê Gestor de Saúde Digital (CGSD)](https://www.gov.br/saude/pt-br/acesso-a-informacao/participacao-social/conselhos-e-orgaos-colegiados/cgsd).

Vale destacar que os perfis terminológicos podem passar por atualizações e versionamentos com periodicidade específica de cada domínio, por isso é importante acompanhar a disponibilização dessas atualizações no projeto [RNDS no Simplifier](https://simplifier.net/redenacionaldedadosemsaude). 

Note que na estrutura dos perfis há elementos com bindings para *ValueSets* que apontam para *CodeSystems*. Já no JSON (`Bundle`), o elemento “*system*” sempre indicará os *CodeSystems* relacionados aos códigos (“*value*”) indicados pelo integrador (autor do registro). 

