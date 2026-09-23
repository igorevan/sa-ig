# Modelo de Informação - Guia de Implementação do Sumário de Alta (SA) da RNDS v1.0.0-release

## Modelo de Informação

### Objetivo

O Sumário de Alta (SA) consiste no documento que contém o relato clínico objetivo sobre as intervenções realizadas, as instruções para continuidade do cuidado pós-alta e o estado de saúde do indivíduo ao final de sua permanência na internação em estabelecimentos de saúde.

### Marcos Legais

*  [Portaria GM/MS Nº 8.026, DE 27 DE agosto DE 2025](https://www.in.gov.br/en/web/dou/-/portaria-gm/ms-n-8.026-de-27-de-agosto-de-2025-651423099) 

### Modelo de Informação

 O modelo de informação é uma representação conceitual e canônica, onde os elementos referentes a um documento específico são modelados em seções e blocos de dados, com seus respectivos tipos de dados a serem informados. Também são apresentadas as referências para o uso de recursos terminológicos, da seguinte maneira: 

*  **Nível**: apresenta o nível do elemento no modelo de informação; 
* **Ocorrência**: descreve o número de vezes (cardinalidade) que o elemento deve/pode aparecer:
*  **Seção/Item**: nome do bloco ou da informação a ser enviada; 
*  **Tipo de dado**: descreve o tipo de dado a ser preenchido; 
*  **Conceito/Observações**: apresenta as definições do elemento; 
*  **Mapeamento Computacional - FHIR**: relaciona o atributo do Modelo Informacional com o Modelo Computacional em FHIR. 

### Blocos do Modelo de Informação

 Segue abaixo o modelo de informação para o Sumário de Alta (SA): 

#### Identificação do indivíduo

| | | | | | |
| :--- | :--- | :--- | :--- | :--- | :--- |
| 1 | [1..1] | Identificação do indivíduo | Seção | Indivíduo: pessoa que recebe o atendimento registrado no contato assistencial. Todos os campos são de preenchimento obrigatório, exceto se o indivíduo não puder ser identificado durante o contato assistencial, sendo preenchida a justificativa da ausência do Cartão Nacional de Saúde (CNS) ou Cadastro de Pessoa Física (CPF). | `Composition [(BRSumarioAlta)](StructureDefinition-BRSumarioAlta.md)``Encounter [(BRContatoAssistencial-1.0)](StructureDefinition-BRContatoAssistencial-1.0.md)``Condition [(BRProblemaDiagnostico](StructureDefinition-BRProblemaDiagnostico.md) e [BRRestricaoFuncionalIncapacidadeSaude-1.0)](StructureDefinition-BRRestricaoFuncionalIncapacidadeSaude-1.0.md)``Procedure [(BRProcedimentoRealizado-1.0)](StructureDefinition-BRProcedimentoRealizado-1.0.md)``ClinicalImpression [(BRResumoEvolucaoClinica)](StructureDefinition-BRResumoEvolucaoClinica.md)``AllergyIntolerance [(BRAlergiaReacaoAdversa-1.0)](StructureDefinition-BRAlergiaReacaoAdversa-1.0.md)``CarePlan [(BRPlanoCuidados-1.0)](StructureDefinition-BRPlanoCuidados-1.0.md)``Observation [(BRObservacaoDescritiva-1.0)](StructureDefinition-BRObservacaoDescritiva-1.0.md)``Composition [(BRRegistroPrescricaoMedicamento)](StructureDefinition-BRRegistroPrescricaoMedicamento.md)``MedicationRequest [(BRPrescricaoMedicamento)](StructureDefinition-BRPrescricaoMedicamento.md)` |
| 2 | [1..1] | Identificador Nacional do Indivíduo | Caracteres numéricos | Identificação unívoca dos usuários das ações e serviços de saúde, com atribuição de um número único válido em todo o território nacional. (Port. nº 940/GM/MS/2011) | `Composition.subject.identifier.value``Encounter.subject.identifier.value``Condition.subject.identifier.value``Procedure.subject.identifier.value``ClinicalImpression.subject.identifier.value``AllergyIntolerance.patient.identifier.value``CarePlan.subject.identifier.value``Observation.subject.identifier.value``Composition.subject.identifier.value``MedicationRequest.subject.identifier.value` |
| 2 | [0..1] | Identificação por dados demográficos |  | Razão pela qual não foi possível obter os dados de identificação do indivíduo no contato assistencial. (Port. nº 84/SAS/MS/1997 e Port. nº02/SAS/SGEP/MS/2012) | `.extension.extension.valueCodeableConcept.coding.code``Composition.subject``Encounter.subject``Condition.subject``Procedure.subject``ClinicalImpression.subject``AllergyIntolerance.patient``CarePlan.subject``Observation.subject` |
| 3 | [1..1] | Data de nascimento | Data conforme ISO 8601 | Estima-se e informa-se apenas o ano de nascimento para contatos assistenciais de indivíduos sem identificação. | `Composition.subject.extension.extension.valueDate``Encounter.subject.extension.extension.valueDate``Condition.subject.extension.extension.valueDate``Procedure.subject.extension.extension.valueDate``ClinicalImpression.subject.extension.extension.valueDate``AllergyIntolerance.patient.extension.extension.valueDate``CarePlan.subject.extension.extension.valueDate``Observation.subject.extension.extension.valueDate` |
| 3 | [1..1] | Sexo | Texto codificado:* Masculino
* Feminino
* Ignorado
 |  | `Composition.subject.extension.extension.valueCode``Encounter.subject.extension.extension.valueCode``Condition.subject.extension.extension.valueCode``Procedure.subject.extension.extension.valueCode``ClinicalImpression.subject.extension.extension.valueCode``AllergyIntolerance.patient.extension.extension.valueCode``CarePlan.subject.extension.extension.valueCode``Observation.subject.extension.extension.valueCode` |
| 1 | [1..1] | Caracterização do atendimento | Seção |  | `Encounter [(BRContatoAssistencial-1.0)](StructureDefinition-BRContatoAssistencial-1.0.md)``Procedure [(BRProcedimentoRealizado-1.0)](StructureDefinition-BRProcedimentoRealizado-1.0.md)``Composition.subject [(BRSumarioAlta)](StructureDefinition-BRSumarioAlta.md)` |
| 2 | [1..1] | Identificador do Estabelecimento de saúde | Caracteres numéricos | Número de identificação no CNES do estabelecimento de saúde que realizou o contato assistencial | `Encounter.serviceProvider.identifier.value` |
| 2 | [1..1] | Procedência | Texto codificado:* Ordem Judicial
* Retorno
* Demanda espontânea
* Demanda referenciada
 | Identifica o serviço que encaminhou o indivíduo ou a sua iniciativa/de seu responsável na busca pelo acesso ao serviço de saúde. | `Encounter.hospitalization.admitSource.coding.code` |
| 2 | [0..1] | Identificação da equipe de saúde | Caracteres numéricos | Número válido do Identificador Nacional de Equipe (INE) no CNES. | `Encounter.participant.extension:team``Procedure.performer.extension.valueInteger` |
| 2 | [1..1] | Caráter da internação | Texto codificado:* Eletiva
* Urgência
 | Identifica a internação de acordo com a prioridade de sua realização. | `Encounter.priority.coding.code` |
| 2 | [1..1] | Data e hora da internação | Data e hora | Conforme ISO 8601. Data e hora da aceitação do indivíduo para início da internação. | `Encounter.period.start` |
| 2 | [1..1] | Modalidade assistencial | Texto codificado:* Atenção Domiciliar
* Atenção Hospitalar
* Atenção Intermediária
* Atenção Psicossocial
* Atenção à Urgência/Emergência
 | Classificação do contato com o serviço de saúde de acordo com as especificidades do modo, local e duração do atendimento. | `Composition.category.coding.code``Encounter.class.code` |
| 1 | [1..1] | Motivo da admissão, diagnósticos relevantes e patologias associadas desenvolvidas na internação | Seção |  | `Condition [(BRProblemaDiagnostico)](StructureDefinition-BRProblemaDiagnostico.md)``Encounter [(BRContatoAssistencial-1.0)](StructureDefinition-BRContatoAssistencial-1.0.md)` |
| 2 | [1..N] | Diagnósticos |  |  |  |
| 3 | [1..1] | Código do Diagnóstico | Texto codificado por terminologia externa |  | `Condition.code.coding.code` |
| 3 | [1..1] | Terminologia que descreve o diagnóstico | Identificador único do objeto:CID-10 | Identificador da terminologia que será utilizada para informar os problemas/diagnósticos avaliados | `Condition.code.coding.system` |
| 3 | [1..1] | Categoria do diagnóstico | Texto Codificado:* Principal
* Secundário
 | Condição estabelecida após estudo de forma a esclarecer qual o mais importante ou principal motivo responsável pela demanda do contato assistencial. O diagnóstico primário reflete achados clínicos descobertos durante a permanência do indivíduo no estabelecimento de saúde, podendo, portanto, ser diferente do diagnóstico de admissão. (Port. nº 1.324/SAS/MS/2014) | `Encounter.diagnosis.rank` |
| 3 | [1..1] | Indicador de presença na admissão | Texto Codificado:* Sim
* Não
* Desconhecido
 | Identifica se o problema/diagnóstico é previamente conhecido na admissão do indivíduo para o atendimento. | `Encounter.diagnosis.use.coding.code` |
| 3 | [0..1] | Estado de resolução | Texto Codificado:* Ativo
* Recorrente
* Recidiva
* Inativo
* Remissão
* Resolvido
 |  | `Condition.clinicalStatus.coding.code` |
| 1 | [0..1] | Restrições funcionais e incapacidades em saúde | Seção |  | `Condition [(BRRestricaoFuncionalIncapacidadeSaude-1.0)](StructureDefinition-BRRestricaoFuncionalIncapacidadeSaude-1.0.md)` |
| 2 | [1..1] | Restrição funcional ou incapacidade | Texto livre |  | `Condition.code.text` |
| 2 | [1..1] | Status da restrição funcional ou incapacidade | Texto codificado:* Ativo
* Inativo
 |  | `Condition.clinicalStatus.coding.code` |
| 1 | [1..1] | Procedimento (s) realizado (s) ou solicitado (s) | Seção |  | `Procedure [(BRProcedimentoRealizado-1.0)](StructureDefinition-BRProcedimentoRealizado-1.0.md)` |
| 2 | [1..N] | Procedimentos |  |  |  |
| 2 | [1..1] | Terminologia que descreve o procedimento | Identificador único do objeto. Texto codificado:* SIGTAP
* CBHPM
* TUSS
 | Identificador da terminologia que será utilizada para informar o(s) procedimento(s) realizado(s) ou solicitados (s). | `Procedure.code.coding.system` |
| 3 | [1..1] | Procedimento realizado | Texto codificado por terminologia externa:* SIGTAP
* CBHPM
* TUSS
 | Ação de saúde realizada no indivíduo durante o contato assistencial (Número TUSS, ex.). | `Procedure.code.coding.code` |
| 3 | [1..1] | Data da realização | Data conforme ISO 8601 |  | `Procedure.performedDateTime` |
| 3 | [1..1] | Status do procedimento | Texto codificado:* Pré-procedimento
* Em andamento
* Não realizado
* Suspenso
* Cancelado
* Completado
* Desconhecido
* Entrada com erro
 |  | `Procedure.status` |
| 3 | [0..1] | Resultado ou observações do procedimento | Texto livre |  | `Procedure.note` |
| 1 | [1..1] | Resumo da evolução clínica do indivíduo durante a internação | Seção | Resume a evolução clínica durante a internação de um paciente, bem como referencia quaisquer informações adicionais ou complementares para a alta do paciente. | `ClinicalImpression [(BRResumoEvolucaoClinica)](StructureDefinition-BRResumoEvolucaoClinica.md)` |
| 2 | [1..1] | Descrição da evolução clínica do indivíduo durante a internação | Texto livre |  | `ClinicalImpression.summary` |
| 1 | [0..N] | Alergias e/ou reações adversas na internação | Seção | Lista todas as alergias e/ou reações adversas do paciente durante a internação | `AllergyIntolerance [(BRAlergiaReacaoAdversa-1.0)](StructureDefinition-BRAlergiaReacaoAdversa-1.0.md)` |
| 2 | [0..N] | Alergia e/ou reação adversa |  |  |  |
| 3 | [1..1] | Categoria do agente causador da alergia ou reação adversa | Texto codificado:* Alimento
* Medicamento
* Fator Externo/ Ambiental
* Biológico
 |  | `AllergyIntolerance.category` |
| 3 | [1..1] | Agente/substância específica | Texto Codificado:* CBARA
* CATMAT
* Lista vacinas PNI
 |  | `AllergyIntolerance.code` |
| 3 | [0..1] | Manifestação | Texto Codificado:* CBARA
 |  | `AllergyIntolerance.reaction.manifestation` |
| 3 | [0..1] | Grau de certeza | Texto codificado:* Não Confirmado
* Confirmado
* Refutado
* Cancelado por informação errada
 |  | `AllergyIntolerance.verificationStatus` |
| 3 | [0..1] | Criticidade | Texto codificado:* Alta
* Baixa
* Indeterminada
 | Uma indicação do potencial de danos nos órgãos críticos do sistema ou consequência de ameaça à vida. | `AllergyIntolerance.criticality` |
| 3 | [0..1] | Data/hora da instalação da reação adversa | ISO 8601 |  | `AllergyIntolerance.onsetDateTime` |
| 3 | [0..1] | Evolução da alergia/reação adversa | Texto livre |  | `AllergyIntolerance.note` |
| 1 | [1..1] | Prescrição da alta |  |  | `Composition [(BRRegistroPrescricaoMedicamento)](StructureDefinition-BRRegistroPrescricaoMedicamento.md)``MedicationRequest [(BRPrescricaoMedicamento)](StructureDefinition-BRPrescricaoMedicamento.md)``Medication [(BRMedicamento)](StructureDefinition-BRMedicamento.md)` |
| 2 | [0..1] | Medicamentos prescritos na alta (não estruturado) |  |  | `MedicationRequest` |
| 3 | [1..1] | Descrição da prescrição | Texto livre | Descrição da prescrição de medicamentos de forma livre, em texto, podendo ter vários medicamentos no mesmo texto. O profissional prescritor deverá descrever todos os campos necessários a uma prescrição, entre outros elementos relevantes. | `MedicationRequest.dosageInstruction.text` |
| 2 | [0..1] | Medicamentos prescritos na alta (estruturado) |  |  | `MedicationRequest` |
| 3 | [1..1] | Terminologia que descreve o medicamento | Texto Codificado:* ANVISA
* Ontologia Brasileira de Medicamentos (OBM)
* CATMAT
 |  | `Medication.code.coding.system` |
| 4 | [1..N] | Medicamento | Texto codificado por terminologia externa | Indica o nome do princípio ativo, concentração, unidade de medida e forma farmacêutica do medicamento prescrito. |  |
| 5 | [1..1] | Via de administração | Texto codificado por terminologia externa |  | `MedicationRequest.dosageInstruction.route` |
| 5 | [1..1] | Posologia |  |  |  |
| 6 | [0..1] | Posologia não estruturada | Texto livre | Descrição da posologia de medicamento de forma livre, em texto. O profissional prescritor deverá descrever todos os campos necessários a uma posologia, entre outros elementos relevantes. | `MedicationRequest.dosageInstruction.text` |
| 6 | [0..1] | Posologia estruturada |  |  |  |
| 7 | [1..1] | Quantidade da Dose | Caracteres numéricos | Quantidade da unidade de consumo do medicamento prescrito a cada dose. | `MedicationRequest.dosageInstruction.doseAndRate.doseValue` |
| 7 | [1..1] | Unidade de consumo da dose | Texto codificado por terminologia externa | Unidade de consumo do medicamento prescrito (ex.: comprimido, cápsula, aplicação, mL, gota, copo dosador, infusão etc.). | `MedicationRequest.dosageInstruction.doseAndRate.type` |
| 7 | [1..1] | Frequência de uso do medicamento |  |  | `MedicationRequest.dosageInstruction.timing` |
| 8 | [1..1] | Dose única | Boleano | Sim; Não(verdadeiro/falso) |  |
| 8 | [0..1] | Uso contínuo |  | RN09: preenchido obrigatoriamente se "Dose Única" = não/falso. |  |
| 9 | [0..1] | Uso se necessário | Boleano | Sim; Não(verdadeiro/falso) | `MedicationRequest.dosageInstruction.asNeededBoolean` |
| 10 | [1..1] | Descrição da necessidade de uso do medicamento | Texto livre | Descrição de uso do medicamento indicado para o caso de uma necessidade específica (ex.: dor, febre, após tratamento etc.) | `MedicationRequest.note` |
| 9 | [0..1] | Intervalo em horas de cada dose do medicamento | Caracteres numéricos | Intervalo, em horas, de cada uso do medicamento | `MedicationRequest.dosageInstruction.timing.repeat.frequency` |
| 9 | [0..1] | Frequência de doses do medicamento |  |  |  |
| 10 | [1..1] | Repetições de dose para uma mesma unidade de tempo | Caracteres numéricos | Número de doses a cada uso do medicamento (ex.: 1x, 2x, 3x 4x etc.) | `MedicationRequest.dosageInstruction.timing.repeat.count` |
| 10 | [1..1] | Intervalo entre doses | Caracteres numéricos | Descritor quantitativo da unidade de tempo entre doses | `MedicationRequest.dosageInstruction.timing.repeat`Extensão - Intervalo entre doses |
| 10 | [1..1] | Unidade de tempo entre doses | Texto codificado | Unidade de tempo entre doses (ex.: hora, dia, semana, mês etc.). | `MedicationRequest.dosageInstruction.timing.repeat`Extensão - Intervalo entre doses |
| 9 | [0..1] | Turno |  |  |  |
| 10 | [1..1] | Turno do dia | Texto codificado | Manhã, tarde, noite. | `MedicationRequest.dosageInstruction.timing.repeat`Extensão BRTurno |
| 10 | [1..1] | Intervalo entre doses | Caracteres numéricos | Descritor quantitativo da unidade de tempo entre doses | `MedicationRequest.dosageInstruction.timing.repeat`Extensão - Intervalo entre doses |
| 10 | [1..1] | Unidade de tempo entre doses | Texto codificado | Unidade de tempo entre doses (ex.: hora, dia, semana, mês, bimestre, trimestre, quadrimestre, semestre, ano). | `MedicationRequest.dosageInstruction.timing.repeat`Extensão - Intervalo entre doses |
| 7 | [0..1] | Quantidade de medicamento prescrito |  |  |  |
| 8 | [1..1] | Quantidade a ser dispensada por atendimento | Caracteres numéricos |  | `MedicationRequest.dosageInstruction.maxDosePerAdministration` |
| 8 | [1..1] | Unidade de medida do medicamento | Texto codificado | Unidade de medida do medicamento prescrito (ex.: comprimido, cápsula, frasco, caixa etc.). | `MedicationRequest.dosageInstruction.doseAndRate.type` |
| 7 | [0..1] | Duração de uso do medicamento | Caracteres alfanuméricos | Duração conforme ISO 8601 | `MedicationRequest.dispenseRequest.validityPeriod` |
| 7 | [0..1] | Total do tratamento | Caracteres numéricos | Quantidade total de medicamento prescrito. | `MedicationRequest.dispenseRequest.quantity` |
| 7 | [0..1] | Orientações sobre o uso do medicamento | Texto livre |  | `MedicationRequest.dosageInstruction.patientInstruction` |
| 1 | [0..1] | Plano de cuidados, instruções e recomendações (na alta) | Seção | Plano de cuidados, instruções e recomendações na alta do paciente | `CarePlan [(BRPlanoCuidados-1.0)](StructureDefinition-BRPlanoCuidados-1.0.md)` |
| 2 | [1..1] | Descrição do plano de cuidados, instruções e recomendações | Texto livre |  | `CarePlan.description` |
| 1 | [1..1] | Informações da alta | Seção |  | `Encounter [(BRContatoAssistencial-1.0)](StructureDefinition-BRContatoAssistencial-1.0.md)` |
| 2 | [1..1] | Data e hora do desfecho da internação | Data e hora | Conforme ISO 8601. Data e hora da alta do paciente | `Encounter.period.end` |
| 2 | [1..1] | Desfecho da internação | Texto codificado:* Alta clínica
* Alta voluntária
* Encaminhamento
* Evasão
* Óbito
* Ordem Judicial
* Permanência
* Retorno
* Transferência
 | Caracteriza o motivo de conclusão da internação. | `Encounter.hospitalization.dischargeDisposition.coding.code` |
| 2 | [0..1] | Encaminhamento pós-alta |  |  |  |
| 3 | [0..1] | Tipo de estabelecimento de saúde | Caracteres numéricos | CNES válido. |  |
| 3 | [0..1] | Descrição do serviço ou especialidade | Texto livre |  |  |
| 2 | [0..1] | Profissional responsável pela alta |  |  | `Encounter.participant` |
| 3 | [1..1] | CNS do profissional | Caracteres numéricos. | CNS válido do profissional responsável pela alta. | `Encounter.participant.identifier.value` |
| 3 | [1..1] | Ocupação do profissional responsável pela alta | Texto codificado por terminologia externa:* CBO MTE
 | Atividade desempenhada pelo profissional responsável pela alta. | `Encounter.participant.extension:function` |
| 1 | [0..1] | Informações Adicionais/Complementares |  |  | `Observation [(BRObservacaoDescritiva-1.0)](StructureDefinition-BRObservacaoDescritiva-1.0.md)``Encounter [(BRContatoAssistencial-1.0)](StructureDefinition-BRContatoAssistencial-1.0.md)` |
| 2 | [1..1] | Descrição das informações | Texto livre | Este campo é destinado às informações relevantes em texto livre para a continuidade do cuidado, como resultados de exames, principais terapias medicamentosas usadas, etc, observando que este não deve ser utilizado em substituição aos blocos de informações disponíveis em outros campos do sumário de alta. | `Observation.valueString``Encounter.hospitalization.extension:otherInformations`Representa quaisquer outras informações descritivas relacionadas aos dados de desfecho do atendimento registrado. |

