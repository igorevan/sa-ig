# Modelo Computacional - Guia de Implementação do Sumário de Alta (SA) da RNDS v1.0.0-release

## Modelo Computacional

### Modelo Computacional

 Para a modelagem dos modelos computacionais do Registros de Imunobiológico Administrado (RIA), foram mapeados os campos do Modelo de Informação (MI) aos recursos internacionais [FHIR R4](https://hl7.org/fhir/R4/). Assim, foi realizada a modelagem fechada dos perfis de modo a atender o contexto nacional. 

Foi criado um [Projeto Rede Nacional de Dados em Saúde](https://simplifier.net/redenacionaldedadosemsaude/), na plataforma [SIMPLIFIER.NET](https://simplifier.net/), para a publicação e distribuição dos perfis relacionados aos documentos computacionais em produção na rede.

### Bundles de Envios do RIA-R

O diagrama abaixo apresenta o pacote *Bundle* no qual é condensado o Registro de Imunobiológico Administrado em Rotina (RIA-R), referenciando todos os dados relevantes para caracterizar uma imunização.

 **Figura 1 - Diagrama do *Bundle* do RIA-R** 

### Recursos FHIR

 O modelo computacional do RIA-R é definido pelo perfil Registro Imunobiológico Administrado na Rotina (RIA-R) [`Composition`].

| | |
| :--- | :--- |
| *Composition* | ` [BRRegistroImunobiologicoAdministradoRotina-2.0](StructureDefinition-BRRegistroImunobiologicoAdministradoRotina-2.0.md) ` |
| *Immunization* | ` [BRImunobiologicoAdministrado-3.0](StructureDefinition-BRImunobiologicoAdministrado-3.0.md) ` |
| *Condition* | ` [BRCID10Avaliado-1.0](StructureDefinition-BRCID10Avaliado-1.0.md) ` |

Extensões utilizadas:

| | |
| :--- | :--- |
| *StructureDefinition* | ` [BRGrupoAtendimento](StructureDefinition-BRGrupoAtendimento.md) ` |
| *StructureDefinition* | ` [BRCondicaoMaternal](StructureDefinition-BRCondicaoMaternal.md) ` |
| *StructureDefinition* | ` [BRContatoHanseniase](StructureDefinition-BRContatoHanseniase.md) ` |
| *StructureDefinition* | ` [BREstrategiaVacinacao-1.0](StructureDefinition-BREstrategiaVacinacao-1.0.md) ` |
| *StructureDefinition* | ` [BREstrategiaVacinacaoPesquisa-1.0](StructureDefinition-BREstrategiaVacinacaoPesquisa-1.0.md) ` |

Perfis dos tipos *ValueSet* e *CodeSystem* estão associados a recursos terminológicos. No contexto de imunizações e os domínios utilizados, foram criados * CodeSystems* específicos definidos pelo [Comitê Gestor de Saúde Digital (CGSD)](https://www.gov.br/saude/pt-br/acesso-a-informacao/participacao-social/conselhos-e-orgaos-colegiados/cgsd).

Vale destacar que os perfis terminológicos podem passar por atualizações e versionamentos com periodicidade específica de cada domínio, por isso é importante acompanhar a disponibilização dessas atualizações no projeto [RNDS no Simplifier](https://simplifier.net/redenacionaldedadosemsaude). 

Note que na estrutura dos perfis há elementos com bindings para *ValueSets* que apontam para *CodeSystems*. Já no JSON (`Bundle`), o elemento “*system*” sempre indicará os *CodeSystems* relacionados aos códigos (“*value*”) indicados pelo integrador (autor do registro). 

| | |
| :--- | :--- |
| `[BRTipoDocumento-1.0](ValueSet-BRTipoDocumento-1.0.md)` | `[BRTipoDocumento](CodeSystem-BRTipoDocumento.md)` |
| `[BROcupacao-1.0](ValueSet-BROcupacao-1.0.md)` | `[BRCBO](CodeSystem-BRCBO.md)` |
| `[BRGrupoAtendimento-1.0](ValueSet-BRGrupoAtendimento-1.0.md)` | `[BRGrupoAtendimento](CodeSystem-BRGrupoAtendimento.md)` |
| `[BRCondicaoMaternal-1.0](ValueSet-BRCondicaoMaternal-1.0.md)` | `[BRCondicaoMaternal](CodeSystem-BRCondicaoMaternal.md)` |
| `[BREstadoEvento-1.0](ValueSet-BREstadoEvento-1.0.md)` | `[event-status](http://hl7.org/fhir/event-status)` |
| `[BRImunobiologico-1.0](ValueSet-BRImunobiologico-1.0.md)` | `[BRImunobiologico](CodeSystem-BRImunobiologico.md)` |
| `[BRRegistroOrigem](ValueSet-BRRegistroOrigem.md)` | `[BRRegistroOrigem](CodeSystem-BRRegistroOrigem.md)` |
| `[BRPais-1.0](ValueSet-BRPais-1.0.md)` | `[BRPais](CodeSystem-BRPais.md)` |
| `[BRFabricanteImunobiologico-1.0](ValueSet-BRFabricanteImunobiologico-1.0.md)` | `[BRFabricantePNI](CodeSystem-BRFabricantePNI.md)` |
| `[BRLocalAplicacao-1.0](ValueSet-BRLocalAplicacao-1.0.md)` | `[BRLocalAplicacao](CodeSystem-BRLocalAplicacao.md)` |
| `[BRViaAdministracao-1.0](ValueSet-BRViaAdministracao-1.0.md)` | `[BRViaAdministracao](CodeSystem-BRViaAdministracao.md)` |
| `[BREstrategiaVacinacao-1.0](ValueSet-BREstrategiaVacinacao-1.0.md)` | `[BREstrategiaVacinacao](CodeSystem-BREstrategiaVacinacao.md)` |
| `[BRDose-1.0](ValueSet-BRDose-1.0.md)` | `[BRDose](CodeSystem-BRDose.md)` |
| `[BREstadoResolucaoDiagnosticoProblema-1.0](ValueSet-BREstadoResolucaoDiagnosticoProblema-1.0.md)` | `[condition-clinical](http://terminology.hl7.org/CodeSystem/condition-clinical)` |
| `[BRCategoriaDiagnostico](ValueSet-BRCategoriaDiagnostico.md)` | `[BRCategoriaDiagnostico](CodeSystem-BRCategoriaDiagnostico.md)` |
| `[BRCID10-1.0](ValueSet-BRCID10-1.0.md)` | `[BRCID10](CodeSystem-BRCID10.md)` |

