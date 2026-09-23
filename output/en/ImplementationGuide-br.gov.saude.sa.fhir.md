# Resource Guia de Implementação do Sumário de Alta (SA) da RNDS



## Resource Content

```json
{
  "resourceType" : "ImplementationGuide",
  "id" : "br.gov.saude.sa.fhir",
  "language" : "en",
  "extension" : [{
    "url" : "http://hl7.org/fhir/StructureDefinition/structuredefinition-standards-status",
    "valueCode" : "normative"
  },
  {
    "url" : "http://hl7.org/fhir/StructureDefinition/structuredefinition-fmm",
    "valueInteger" : 1
  },
  {
    "url" : "http://hl7.org/fhir/StructureDefinition/structuredefinition-wg",
    "valueCode" : "ehr"
  },
  {
    "url" : "http://hl7.org/fhir/StructureDefinition/structuredefinition-normative-version",
    "valueCode" : "4.0.1"
  }],
  "url" : "https://fhir.saude.gov.br/sa/ImplementationGuide/br.gov.saude.sa.fhir",
  "version" : "1.0.0-release",
  "name" : "SARNDSIG",
  "title" : "Guia de Implementação do Sumário de Alta (SA) da RNDS",
  "status" : "active",
  "experimental" : false,
  "date" : "2026-09-22T22:11:28-03:00",
  "publisher" : "Ministério da Saúde do Brasil",
  "contact" : [{
    "name" : "Ministério da Saúde do Brasil",
    "telecom" : [{
      "system" : "url",
      "value" : "http://www.saude.gov.br"
    },
    {
      "system" : "email",
      "value" : "cgiis.datasus@saude.gov.br"
    }]
  }],
  "description" : "Guia de Implementação da Rede Nacional de Dados em Saúde (RNDS)",
  "jurisdiction" : [{
    "coding" : [{
      "system" : "urn:iso:std:iso:3166",
      "code" : "BR"
    }]
  }],
  "packageId" : "br.gov.saude.sa.fhir",
  "license" : "CC0-1.0",
  "fhirVersion" : ["4.0.1"],
  "dependsOn" : [{
    "id" : "hl7tx",
    "extension" : [{
      "url" : "http://hl7.org/fhir/tools/StructureDefinition/implementationguide-dependency-comment",
      "valueMarkdown" : "Automatically added as a dependency - all IGs depend on HL7 Terminology"
    }],
    "uri" : "http://terminology.hl7.org/ImplementationGuide/hl7.terminology",
    "packageId" : "hl7.terminology.r4",
    "version" : "7.4.0"
  },
  {
    "id" : "hl7ext",
    "extension" : [{
      "url" : "http://hl7.org/fhir/tools/StructureDefinition/implementationguide-dependency-comment",
      "valueMarkdown" : "Automatically added as a dependency - all IGs depend on the HL7 Extension Pack"
    }],
    "uri" : "http://hl7.org/fhir/extensions/ImplementationGuide/hl7.fhir.uv.extensions",
    "packageId" : "hl7.fhir.uv.extensions.r4",
    "version" : "5.3.0"
  }],
  "definition" : {
    "extension" : [{
      "extension" : [{
        "url" : "code",
        "valueString" : "copyrightyear"
      },
      {
        "url" : "value",
        "valueString" : "2026+"
      }],
      "url" : "http://hl7.org/fhir/tools/StructureDefinition/ig-parameter"
    },
    {
      "extension" : [{
        "url" : "code",
        "valueString" : "releaselabel"
      },
      {
        "url" : "value",
        "valueString" : "STU1"
      }],
      "url" : "http://hl7.org/fhir/tools/StructureDefinition/ig-parameter"
    },
    {
      "extension" : [{
        "url" : "code",
        "valueString" : "shownav"
      },
      {
        "url" : "value",
        "valueString" : "true"
      }],
      "url" : "http://hl7.org/fhir/tools/StructureDefinition/ig-parameter"
    },
    {
      "extension" : [{
        "url" : "code",
        "valueString" : "special-url-base"
      },
      {
        "url" : "value",
        "valueString" : "http://www.saude.gov.br/fhir/r4"
      }],
      "url" : "http://hl7.org/fhir/tools/StructureDefinition/ig-parameter"
    },
    {
      "extension" : [{
        "url" : "code",
        "valueString" : "autoload-resources"
      },
      {
        "url" : "value",
        "valueString" : "true"
      }],
      "url" : "http://hl7.org/fhir/tools/StructureDefinition/ig-parameter"
    },
    {
      "extension" : [{
        "url" : "code",
        "valueString" : "path-liquid-template"
      },
      {
        "url" : "value",
        "valueString" : "template/liquid"
      }],
      "url" : "http://hl7.org/fhir/tools/StructureDefinition/ig-parameter"
    },
    {
      "extension" : [{
        "url" : "code",
        "valueString" : "path-liquid-template"
      },
      {
        "url" : "value",
        "valueString" : "input/liquid"
      }],
      "url" : "http://hl7.org/fhir/tools/StructureDefinition/ig-parameter"
    },
    {
      "extension" : [{
        "url" : "code",
        "valueString" : "path-qa"
      },
      {
        "url" : "value",
        "valueString" : "temp/qa"
      }],
      "url" : "http://hl7.org/fhir/tools/StructureDefinition/ig-parameter"
    },
    {
      "extension" : [{
        "url" : "code",
        "valueString" : "path-temp"
      },
      {
        "url" : "value",
        "valueString" : "temp/pages"
      }],
      "url" : "http://hl7.org/fhir/tools/StructureDefinition/ig-parameter"
    },
    {
      "extension" : [{
        "url" : "code",
        "valueString" : "path-output"
      },
      {
        "url" : "value",
        "valueString" : "output"
      }],
      "url" : "http://hl7.org/fhir/tools/StructureDefinition/ig-parameter"
    },
    {
      "extension" : [{
        "url" : "code",
        "valueString" : "path-suppressed-warnings"
      },
      {
        "url" : "value",
        "valueString" : "input/ignoreWarnings.txt"
      }],
      "url" : "http://hl7.org/fhir/tools/StructureDefinition/ig-parameter"
    },
    {
      "extension" : [{
        "url" : "code",
        "valueString" : "path-history"
      },
      {
        "url" : "value",
        "valueString" : "https://fhir.saude.gov.br/sa/history.html"
      }],
      "url" : "http://hl7.org/fhir/tools/StructureDefinition/ig-parameter"
    },
    {
      "extension" : [{
        "url" : "code",
        "valueString" : "template-html"
      },
      {
        "url" : "value",
        "valueString" : "template-page.html"
      }],
      "url" : "http://hl7.org/fhir/tools/StructureDefinition/ig-parameter"
    },
    {
      "extension" : [{
        "url" : "code",
        "valueString" : "template-md"
      },
      {
        "url" : "value",
        "valueString" : "template-page-md.html"
      }],
      "url" : "http://hl7.org/fhir/tools/StructureDefinition/ig-parameter"
    },
    {
      "extension" : [{
        "url" : "code",
        "valueString" : "apply-contact"
      },
      {
        "url" : "value",
        "valueString" : "true"
      }],
      "url" : "http://hl7.org/fhir/tools/StructureDefinition/ig-parameter"
    },
    {
      "extension" : [{
        "url" : "code",
        "valueString" : "apply-context"
      },
      {
        "url" : "value",
        "valueString" : "true"
      }],
      "url" : "http://hl7.org/fhir/tools/StructureDefinition/ig-parameter"
    },
    {
      "extension" : [{
        "url" : "code",
        "valueString" : "apply-copyright"
      },
      {
        "url" : "value",
        "valueString" : "true"
      }],
      "url" : "http://hl7.org/fhir/tools/StructureDefinition/ig-parameter"
    },
    {
      "extension" : [{
        "url" : "code",
        "valueString" : "apply-jurisdiction"
      },
      {
        "url" : "value",
        "valueString" : "true"
      }],
      "url" : "http://hl7.org/fhir/tools/StructureDefinition/ig-parameter"
    },
    {
      "extension" : [{
        "url" : "code",
        "valueString" : "apply-license"
      },
      {
        "url" : "value",
        "valueString" : "true"
      }],
      "url" : "http://hl7.org/fhir/tools/StructureDefinition/ig-parameter"
    },
    {
      "extension" : [{
        "url" : "code",
        "valueString" : "apply-publisher"
      },
      {
        "url" : "value",
        "valueString" : "true"
      }],
      "url" : "http://hl7.org/fhir/tools/StructureDefinition/ig-parameter"
    },
    {
      "extension" : [{
        "url" : "code",
        "valueString" : "apply-version"
      },
      {
        "url" : "value",
        "valueString" : "true"
      }],
      "url" : "http://hl7.org/fhir/tools/StructureDefinition/ig-parameter"
    },
    {
      "extension" : [{
        "url" : "code",
        "valueString" : "apply-wg"
      },
      {
        "url" : "value",
        "valueString" : "true"
      }],
      "url" : "http://hl7.org/fhir/tools/StructureDefinition/ig-parameter"
    },
    {
      "extension" : [{
        "url" : "code",
        "valueString" : "active-tables"
      },
      {
        "url" : "value",
        "valueString" : "true"
      }],
      "url" : "http://hl7.org/fhir/tools/StructureDefinition/ig-parameter"
    },
    {
      "extension" : [{
        "url" : "code",
        "valueString" : "fmm-definition"
      },
      {
        "url" : "value",
        "valueString" : "http://hl7.org/fhir/versions.html#maturity"
      }],
      "url" : "http://hl7.org/fhir/tools/StructureDefinition/ig-parameter"
    },
    {
      "extension" : [{
        "url" : "code",
        "valueString" : "propagate-status"
      },
      {
        "url" : "value",
        "valueString" : "true"
      }],
      "url" : "http://hl7.org/fhir/tools/StructureDefinition/ig-parameter"
    },
    {
      "extension" : [{
        "url" : "code",
        "valueString" : "excludelogbinaryformat"
      },
      {
        "url" : "value",
        "valueString" : "true"
      }],
      "url" : "http://hl7.org/fhir/tools/StructureDefinition/ig-parameter"
    },
    {
      "extension" : [{
        "url" : "code",
        "valueString" : "tabbed-snapshots"
      },
      {
        "url" : "value",
        "valueString" : "true"
      }],
      "url" : "http://hl7.org/fhir/tools/StructureDefinition/ig-parameter"
    },
    {
      "extension" : [{
        "url" : "code",
        "valueString" : "i18n-default-lang"
      },
      {
        "url" : "value",
        "valueString" : "en"
      }],
      "url" : "http://hl7.org/fhir/tools/StructureDefinition/ig-parameter"
    },
    {
      "url" : "http://hl7.org/fhir/tools/StructureDefinition/ig-internal-dependency",
      "valueCode" : "hl7.fhir.uv.tools.r4#1.1.2"
    },
    {
      "extension" : [{
        "url" : "code",
        "valueCode" : "copyrightyear"
      },
      {
        "url" : "value",
        "valueString" : "2026+"
      }],
      "url" : "http://hl7.org/fhir/tools/StructureDefinition/ig-parameter"
    },
    {
      "extension" : [{
        "url" : "code",
        "valueCode" : "releaselabel"
      },
      {
        "url" : "value",
        "valueString" : "STU1"
      }],
      "url" : "http://hl7.org/fhir/tools/StructureDefinition/ig-parameter"
    },
    {
      "extension" : [{
        "url" : "code",
        "valueCode" : "shownav"
      },
      {
        "url" : "value",
        "valueString" : "true"
      }],
      "url" : "http://hl7.org/fhir/tools/StructureDefinition/ig-parameter"
    },
    {
      "extension" : [{
        "url" : "code",
        "valueCode" : "special-url-base"
      },
      {
        "url" : "value",
        "valueString" : "http://www.saude.gov.br/fhir/r4"
      }],
      "url" : "http://hl7.org/fhir/tools/StructureDefinition/ig-parameter"
    },
    {
      "extension" : [{
        "url" : "code",
        "valueCode" : "autoload-resources"
      },
      {
        "url" : "value",
        "valueString" : "true"
      }],
      "url" : "http://hl7.org/fhir/tools/StructureDefinition/ig-parameter"
    },
    {
      "extension" : [{
        "url" : "code",
        "valueCode" : "path-liquid-template"
      },
      {
        "url" : "value",
        "valueString" : "template/liquid"
      }],
      "url" : "http://hl7.org/fhir/tools/StructureDefinition/ig-parameter"
    },
    {
      "extension" : [{
        "url" : "code",
        "valueCode" : "path-liquid-template"
      },
      {
        "url" : "value",
        "valueString" : "input/liquid"
      }],
      "url" : "http://hl7.org/fhir/tools/StructureDefinition/ig-parameter"
    },
    {
      "extension" : [{
        "url" : "code",
        "valueCode" : "path-qa"
      },
      {
        "url" : "value",
        "valueString" : "temp/qa"
      }],
      "url" : "http://hl7.org/fhir/tools/StructureDefinition/ig-parameter"
    },
    {
      "extension" : [{
        "url" : "code",
        "valueCode" : "path-temp"
      },
      {
        "url" : "value",
        "valueString" : "temp/pages"
      }],
      "url" : "http://hl7.org/fhir/tools/StructureDefinition/ig-parameter"
    },
    {
      "extension" : [{
        "url" : "code",
        "valueCode" : "path-output"
      },
      {
        "url" : "value",
        "valueString" : "output"
      }],
      "url" : "http://hl7.org/fhir/tools/StructureDefinition/ig-parameter"
    },
    {
      "extension" : [{
        "url" : "code",
        "valueCode" : "path-suppressed-warnings"
      },
      {
        "url" : "value",
        "valueString" : "input/ignoreWarnings.txt"
      }],
      "url" : "http://hl7.org/fhir/tools/StructureDefinition/ig-parameter"
    },
    {
      "extension" : [{
        "url" : "code",
        "valueCode" : "path-history"
      },
      {
        "url" : "value",
        "valueString" : "https://fhir.saude.gov.br/sa/history.html"
      }],
      "url" : "http://hl7.org/fhir/tools/StructureDefinition/ig-parameter"
    },
    {
      "extension" : [{
        "url" : "code",
        "valueCode" : "template-html"
      },
      {
        "url" : "value",
        "valueString" : "template-page.html"
      }],
      "url" : "http://hl7.org/fhir/tools/StructureDefinition/ig-parameter"
    },
    {
      "extension" : [{
        "url" : "code",
        "valueCode" : "template-md"
      },
      {
        "url" : "value",
        "valueString" : "template-page-md.html"
      }],
      "url" : "http://hl7.org/fhir/tools/StructureDefinition/ig-parameter"
    },
    {
      "extension" : [{
        "url" : "code",
        "valueCode" : "apply-contact"
      },
      {
        "url" : "value",
        "valueString" : "true"
      }],
      "url" : "http://hl7.org/fhir/tools/StructureDefinition/ig-parameter"
    },
    {
      "extension" : [{
        "url" : "code",
        "valueCode" : "apply-context"
      },
      {
        "url" : "value",
        "valueString" : "true"
      }],
      "url" : "http://hl7.org/fhir/tools/StructureDefinition/ig-parameter"
    },
    {
      "extension" : [{
        "url" : "code",
        "valueCode" : "apply-copyright"
      },
      {
        "url" : "value",
        "valueString" : "true"
      }],
      "url" : "http://hl7.org/fhir/tools/StructureDefinition/ig-parameter"
    },
    {
      "extension" : [{
        "url" : "code",
        "valueCode" : "apply-jurisdiction"
      },
      {
        "url" : "value",
        "valueString" : "true"
      }],
      "url" : "http://hl7.org/fhir/tools/StructureDefinition/ig-parameter"
    },
    {
      "extension" : [{
        "url" : "code",
        "valueCode" : "apply-license"
      },
      {
        "url" : "value",
        "valueString" : "true"
      }],
      "url" : "http://hl7.org/fhir/tools/StructureDefinition/ig-parameter"
    },
    {
      "extension" : [{
        "url" : "code",
        "valueCode" : "apply-publisher"
      },
      {
        "url" : "value",
        "valueString" : "true"
      }],
      "url" : "http://hl7.org/fhir/tools/StructureDefinition/ig-parameter"
    },
    {
      "extension" : [{
        "url" : "code",
        "valueCode" : "apply-version"
      },
      {
        "url" : "value",
        "valueString" : "true"
      }],
      "url" : "http://hl7.org/fhir/tools/StructureDefinition/ig-parameter"
    },
    {
      "extension" : [{
        "url" : "code",
        "valueCode" : "apply-wg"
      },
      {
        "url" : "value",
        "valueString" : "true"
      }],
      "url" : "http://hl7.org/fhir/tools/StructureDefinition/ig-parameter"
    },
    {
      "extension" : [{
        "url" : "code",
        "valueCode" : "active-tables"
      },
      {
        "url" : "value",
        "valueString" : "true"
      }],
      "url" : "http://hl7.org/fhir/tools/StructureDefinition/ig-parameter"
    },
    {
      "extension" : [{
        "url" : "code",
        "valueCode" : "fmm-definition"
      },
      {
        "url" : "value",
        "valueString" : "http://hl7.org/fhir/versions.html#maturity"
      }],
      "url" : "http://hl7.org/fhir/tools/StructureDefinition/ig-parameter"
    },
    {
      "extension" : [{
        "url" : "code",
        "valueCode" : "propagate-status"
      },
      {
        "url" : "value",
        "valueString" : "true"
      }],
      "url" : "http://hl7.org/fhir/tools/StructureDefinition/ig-parameter"
    },
    {
      "extension" : [{
        "url" : "code",
        "valueCode" : "excludelogbinaryformat"
      },
      {
        "url" : "value",
        "valueString" : "true"
      }],
      "url" : "http://hl7.org/fhir/tools/StructureDefinition/ig-parameter"
    },
    {
      "extension" : [{
        "url" : "code",
        "valueCode" : "tabbed-snapshots"
      },
      {
        "url" : "value",
        "valueString" : "true"
      }],
      "url" : "http://hl7.org/fhir/tools/StructureDefinition/ig-parameter"
    },
    {
      "extension" : [{
        "url" : "code",
        "valueCode" : "i18n-default-lang"
      },
      {
        "url" : "value",
        "valueString" : "en"
      }],
      "url" : "http://hl7.org/fhir/tools/StructureDefinition/ig-parameter"
    }],
    "resource" : [{
      "extension" : [{
        "url" : "http://hl7.org/fhir/tools/StructureDefinition/resource-information",
        "valueString" : "Bundle"
      },
      {
        "url" : "http://hl7.org/fhir/StructureDefinition/implementationguide-page",
        "valueUri" : "Bundle-example-SA.html"
      }],
      "reference" : {
        "reference" : "Bundle/example-SA"
      },
      "name" : "Bundle de exemplo do SA",
      "description" : "Bundle de exemplo do Sumário de Alta (SA)",
      "exampleCanonical" : "http://www.saude.gov.br/fhir/r4/StructureDefinition/BRSumarioAlta"
    },
    {
      "extension" : [{
        "url" : "http://hl7.org/fhir/tools/StructureDefinition/resource-information",
        "valueString" : "CodeSystem"
      },
      {
        "url" : "http://hl7.org/fhir/StructureDefinition/implementationguide-page",
        "valueUri" : "CodeSystem-BRAlergenosCBARA.html"
      }],
      "reference" : {
        "reference" : "CodeSystem/BRAlergenosCBARA"
      },
      "name" : "Catálogo Brasileiro de Alergias e Reações Adversas (CBARA)",
      "description" : "Classifica as alergias e reações adversas."
    },
    {
      "extension" : [{
        "url" : "http://hl7.org/fhir/tools/StructureDefinition/resource-information",
        "valueString" : "CodeSystem"
      },
      {
        "url" : "http://hl7.org/fhir/StructureDefinition/implementationguide-page",
        "valueUri" : "CodeSystem-BRCBHPMTUSS.html"
      }],
      "reference" : {
        "reference" : "CodeSystem/BRCBHPMTUSS"
      },
      "name" : "Classificação Brasileira Hierarquizada de Procedimentos Médicos - CBHPM e da Terminologia Unificada da Saúde Suplementar - TUSS",
      "description" : "Classificações de procedimentos utilizadas no Brasil, no contexto da assistência à saúde privada, não complementar ao SUS, e eventualmente no SUS para classificar procedimento inexistente na Tabela SUS."
    },
    {
      "extension" : [{
        "url" : "http://hl7.org/fhir/tools/StructureDefinition/resource-information",
        "valueString" : "CodeSystem"
      },
      {
        "url" : "http://hl7.org/fhir/StructureDefinition/implementationguide-page",
        "valueUri" : "CodeSystem-BRCBO.html"
      }],
      "reference" : {
        "reference" : "CodeSystem/BRCBO"
      },
      "name" : "Classificação Brasileira de Ocupações - CBO (CodeSystem)",
      "description" : "Classifica as profissões do mercado de trabalho brasileiro."
    },
    {
      "extension" : [{
        "url" : "http://hl7.org/fhir/tools/StructureDefinition/resource-information",
        "valueString" : "CodeSystem"
      },
      {
        "url" : "http://hl7.org/fhir/StructureDefinition/implementationguide-page",
        "valueUri" : "CodeSystem-BRCIAP2.html"
      }],
      "reference" : {
        "reference" : "CodeSystem/BRCIAP2"
      },
      "name" : "Classificação Internacional de Atenção Primária - Segunda Edição - CIAP2",
      "description" : "Classifica os problemas identificados no contato assistencial pelos profissionais de saúde, os motivos da contato assistencial e as respostas propostas pela equipe seguindo a sistematização SOAP."
    },
    {
      "extension" : [{
        "url" : "http://hl7.org/fhir/tools/StructureDefinition/resource-information",
        "valueString" : "CodeSystem"
      },
      {
        "url" : "http://hl7.org/fhir/StructureDefinition/implementationguide-page",
        "valueUri" : "CodeSystem-BRCID10.html"
      }],
      "reference" : {
        "reference" : "CodeSystem/BRCID10"
      },
      "name" : "Classificação Internacional de Doenças - Décima Revisão - CID-10",
      "description" : "Classifica as doenças e outros problemas em saúde registrados em diversos tipos de documentos clínicos."
    },
    {
      "extension" : [{
        "url" : "http://hl7.org/fhir/tools/StructureDefinition/resource-information",
        "valueString" : "CodeSystem"
      },
      {
        "url" : "http://hl7.org/fhir/StructureDefinition/implementationguide-page",
        "valueUri" : "CodeSystem-BRCaraterAtendimento.html"
      }],
      "reference" : {
        "reference" : "CodeSystem/BRCaraterAtendimento"
      },
      "name" : "Caráter de Atendimento",
      "description" : "Terminologia que classifica a prioridade de realização de um Contato Assistencial."
    },
    {
      "extension" : [{
        "url" : "http://hl7.org/fhir/tools/StructureDefinition/resource-information",
        "valueString" : "CodeSystem"
      },
      {
        "url" : "http://hl7.org/fhir/StructureDefinition/implementationguide-page",
        "valueUri" : "CodeSystem-BRDadoAusenteOuDesconhecido.html"
      }],
      "reference" : {
        "reference" : "CodeSystem/BRDadoAusenteOuDesconhecido"
      },
      "name" : "Classificação de dados ausentes ou desconhecidos - IPS",
      "description" : "Classificação de dados conhecidos mas ausentes e de dados desconhecidos a partir do International Patient Summary - IPS."
    },
    {
      "extension" : [{
        "url" : "http://hl7.org/fhir/tools/StructureDefinition/resource-information",
        "valueString" : "CodeSystem"
      },
      {
        "url" : "http://hl7.org/fhir/StructureDefinition/implementationguide-page",
        "valueUri" : "CodeSystem-BRFinanciamento.html"
      }],
      "reference" : {
        "reference" : "CodeSystem/BRFinanciamento"
      },
      "name" : "Financiamento (CodeSystem)",
      "description" : "Terminologia que descreve o agente, instituição ou entidade responsável por custear as ações e serviços de saúde."
    },
    {
      "extension" : [{
        "url" : "http://hl7.org/fhir/tools/StructureDefinition/resource-information",
        "valueString" : "CodeSystem"
      },
      {
        "url" : "http://hl7.org/fhir/StructureDefinition/implementationguide-page",
        "valueUri" : "CodeSystem-BRImunobiologico.html"
      }],
      "reference" : {
        "reference" : "CodeSystem/BRImunobiologico"
      },
      "name" : "Imunobiológico (CodeSystem)",
      "description" : "Classifica os tipos de imunobiológicos."
    },
    {
      "extension" : [{
        "url" : "http://hl7.org/fhir/tools/StructureDefinition/resource-information",
        "valueString" : "CodeSystem"
      },
      {
        "url" : "http://hl7.org/fhir/StructureDefinition/implementationguide-page",
        "valueUri" : "CodeSystem-BRJustificativaIndividuoNaoIdentificado.html"
      }],
      "reference" : {
        "reference" : "CodeSystem/BRJustificativaIndividuoNaoIdentificado"
      },
      "name" : "Justificativa da Impossibilidade de Identificação do Indivíduo (CodeSystem)",
      "description" : "Classifica as razões pelo qual não foi possível obter os dados de identificação do indivíduo em um contato assistencial. (Port. nº 84/SAS/MS/1997 e Port. nº02/SAS/SGEP/MS/2012)"
    },
    {
      "extension" : [{
        "url" : "http://hl7.org/fhir/tools/StructureDefinition/resource-information",
        "valueString" : "CodeSystem"
      },
      {
        "url" : "http://hl7.org/fhir/StructureDefinition/implementationguide-page",
        "valueUri" : "CodeSystem-BRMedDRA.html"
      }],
      "reference" : {
        "reference" : "CodeSystem/BRMedDRA"
      },
      "name" : "Medical Dictionary for Regulatory Activities (MedDRA)",
      "description" : "Medical Dictionary for Regulatory Activities."
    },
    {
      "extension" : [{
        "url" : "http://hl7.org/fhir/tools/StructureDefinition/resource-information",
        "valueString" : "CodeSystem"
      },
      {
        "url" : "http://hl7.org/fhir/StructureDefinition/implementationguide-page",
        "valueUri" : "CodeSystem-BRMedicamento.html"
      }],
      "reference" : {
        "reference" : "CodeSystem/BRMedicamento"
      },
      "name" : "Medicamento (CodeSystem)",
      "description" : "Drogas dirigidas para uso humano, apresentadas em sua formulação final."
    },
    {
      "extension" : [{
        "url" : "http://hl7.org/fhir/tools/StructureDefinition/resource-information",
        "valueString" : "CodeSystem"
      },
      {
        "url" : "http://hl7.org/fhir/StructureDefinition/implementationguide-page",
        "valueUri" : "CodeSystem-BRModalidadeAssistencial.html"
      }],
      "reference" : {
        "reference" : "CodeSystem/BRModalidadeAssistencial"
      },
      "name" : "Modalidade Assistencial (CodeSystem)",
      "description" : "Classifica os contatos assistenciais de acordo com as especificidades do modo, local e duração do atendimento"
    },
    {
      "extension" : [{
        "url" : "http://hl7.org/fhir/tools/StructureDefinition/resource-information",
        "valueString" : "CodeSystem"
      },
      {
        "url" : "http://hl7.org/fhir/StructureDefinition/implementationguide-page",
        "valueUri" : "CodeSystem-BRModalidadeTelessaude.html"
      }],
      "reference" : {
        "reference" : "CodeSystem/BRModalidadeTelessaude"
      },
      "name" : "Modalidade de Telessaúde (CodeSystem)",
      "description" : "Códigos para representação da modalidade de telessaúde realizada."
    },
    {
      "extension" : [{
        "url" : "http://hl7.org/fhir/tools/StructureDefinition/resource-information",
        "valueString" : "CodeSystem"
      },
      {
        "url" : "http://hl7.org/fhir/StructureDefinition/implementationguide-page",
        "valueUri" : "CodeSystem-BRMotivoDesfecho.html"
      }],
      "reference" : {
        "reference" : "CodeSystem/BRMotivoDesfecho"
      },
      "name" : "Motivo do Desfecho",
      "description" : "Caracteriza o motivo de conclusão total ou parcial do contato assistencial."
    },
    {
      "extension" : [{
        "url" : "http://hl7.org/fhir/tools/StructureDefinition/resource-information",
        "valueString" : "CodeSystem"
      },
      {
        "url" : "http://hl7.org/fhir/StructureDefinition/implementationguide-page",
        "valueUri" : "CodeSystem-BRObmAMPP.html"
      }],
      "reference" : {
        "reference" : "CodeSystem/BRObmAMPP"
      },
      "name" : "Terminologia de Produto Medicinal Comercial com Apresentação (AMPP) na Ontologia Brasileira de Medicamentos (OBM)",
      "description" : "Apresenta o Terminologia de Produto Medicinal Comercial com Apresentação (AMPP) e seu Código na Ontologia Brasileira de Medicamentos (OBM)"
    },
    {
      "extension" : [{
        "url" : "http://hl7.org/fhir/tools/StructureDefinition/resource-information",
        "valueString" : "CodeSystem"
      },
      {
        "url" : "http://hl7.org/fhir/StructureDefinition/implementationguide-page",
        "valueUri" : "CodeSystem-BRObmANVISA.html"
      }],
      "reference" : {
        "reference" : "CodeSystem/BRObmANVISA"
      },
      "name" : "Terminologia de Produto Medicinal Comercial com Apresentação (AMPP) na Agência Nacional de Vigilância Sanitária (Anvisa)",
      "description" : "Apresenta o Produto Medicinal Comercial com Apresentação (AMPP) e seu Código de Registro na Agência Nacional de Vigilância Sanitária (Anvisa)"
    },
    {
      "extension" : [{
        "url" : "http://hl7.org/fhir/tools/StructureDefinition/resource-information",
        "valueString" : "CodeSystem"
      },
      {
        "url" : "http://hl7.org/fhir/StructureDefinition/implementationguide-page",
        "valueUri" : "CodeSystem-BRObmCATMAT.html"
      }],
      "reference" : {
        "reference" : "CodeSystem/BRObmCATMAT"
      },
      "name" : "Terminologia de Produto Medicinal Virtual (VMP) no Catálogo de Materiais (CATMAT)",
      "description" : "Apresenta o Produto Medicinal Virtual (VMP) e seu código no Catálogo de Materiais (CATMAT)"
    },
    {
      "extension" : [{
        "url" : "http://hl7.org/fhir/tools/StructureDefinition/resource-information",
        "valueString" : "CodeSystem"
      },
      {
        "url" : "http://hl7.org/fhir/StructureDefinition/implementationguide-page",
        "valueUri" : "CodeSystem-BRObmEAN.html"
      }],
      "reference" : {
        "reference" : "CodeSystem/BRObmEAN"
      },
      "name" : "Terminologia de Produto Medicinal Virtual (VMP) na GS1.org",
      "description" : "Apresenta o Produto Medicinal Virtual (VMP) e seu Número Europeu do Artigo (EAN) na GS1.org"
    },
    {
      "extension" : [{
        "url" : "http://hl7.org/fhir/tools/StructureDefinition/resource-information",
        "valueString" : "CodeSystem"
      },
      {
        "url" : "http://hl7.org/fhir/StructureDefinition/implementationguide-page",
        "valueUri" : "CodeSystem-BRObmVMP.html"
      }],
      "reference" : {
        "reference" : "CodeSystem/BRObmVMP"
      },
      "name" : "Terminologia de Produto Medicinal Virtual (VMP) na Ontologia Brasileira de Medicamentos (OBM)",
      "description" : "Apresenta o Produto Medicinal Virtual (VMP) e seu Código na Ontologia Brasileira de Medicamentos (OBM)"
    },
    {
      "extension" : [{
        "url" : "http://hl7.org/fhir/tools/StructureDefinition/resource-information",
        "valueString" : "CodeSystem"
      },
      {
        "url" : "http://hl7.org/fhir/StructureDefinition/implementationguide-page",
        "valueUri" : "CodeSystem-BRPapelProblemaDiagnostico.html"
      }],
      "reference" : {
        "reference" : "CodeSystem/BRPapelProblemaDiagnostico"
      },
      "name" : "Classificação do papel de um problema e diagnóstico (CodeSystem)",
      "description" : "Classificação do papel de um problema/diagnóstico."
    },
    {
      "extension" : [{
        "url" : "http://hl7.org/fhir/tools/StructureDefinition/resource-information",
        "valueString" : "CodeSystem"
      },
      {
        "url" : "http://hl7.org/fhir/StructureDefinition/implementationguide-page",
        "valueUri" : "CodeSystem-BRProcedencia.html"
      }],
      "reference" : {
        "reference" : "CodeSystem/BRProcedencia"
      },
      "name" : "Procedência",
      "description" : "Identifica o serviço que encaminhou o indivíduo ou a sua iniciativa/de seu responsável na busca pelo acesso ao serviço de saúde."
    },
    {
      "extension" : [{
        "url" : "http://hl7.org/fhir/tools/StructureDefinition/resource-information",
        "valueString" : "CodeSystem"
      },
      {
        "url" : "http://hl7.org/fhir/StructureDefinition/implementationguide-page",
        "valueUri" : "CodeSystem-BRResponsabilidadeParticipante.html"
      }],
      "reference" : {
        "reference" : "CodeSystem/BRResponsabilidadeParticipante"
      },
      "name" : "Responsabilidade no Contato Assistencial",
      "description" : "Classifica o tipo de responsabilidade de indivíduos ou profissionais no Contato Assisntecial."
    },
    {
      "extension" : [{
        "url" : "http://hl7.org/fhir/tools/StructureDefinition/resource-information",
        "valueString" : "CodeSystem"
      },
      {
        "url" : "http://hl7.org/fhir/StructureDefinition/implementationguide-page",
        "valueUri" : "CodeSystem-BRTabelaSUS.html"
      }],
      "reference" : {
        "reference" : "CodeSystem/BRTabelaSUS"
      },
      "name" : "Tabela de procedimentos, medicamentos e OPM do SUS",
      "description" : "Padroniza os códigos e as nomenclaturas dos procedimentos, medicamentos e OPM para as informações trafegadas no SUS"
    },
    {
      "extension" : [{
        "url" : "http://hl7.org/fhir/tools/StructureDefinition/resource-information",
        "valueString" : "CodeSystem"
      },
      {
        "url" : "http://hl7.org/fhir/StructureDefinition/implementationguide-page",
        "valueUri" : "CodeSystem-BRTipoDocumento.html"
      }],
      "reference" : {
        "reference" : "CodeSystem/BRTipoDocumento"
      },
      "name" : "Tipo de Documento (CodeSystem)",
      "description" : "Classificação dos tipos de documentos compartilhados no Brasil."
    },
    {
      "extension" : [{
        "url" : "http://hl7.org/fhir/tools/StructureDefinition/resource-information",
        "valueString" : "CodeSystem"
      },
      {
        "url" : "http://hl7.org/fhir/StructureDefinition/implementationguide-page",
        "valueUri" : "CodeSystem-BRTipoIdentificador.html"
      }],
      "reference" : {
        "reference" : "CodeSystem/BRTipoIdentificador"
      },
      "name" : "Tipo de Identificador",
      "description" : "Classifica o tipo de indicador que está sendo utilizado."
    },
    {
      "extension" : [{
        "url" : "http://hl7.org/fhir/tools/StructureDefinition/resource-information",
        "valueString" : "CodeSystem"
      },
      {
        "url" : "http://hl7.org/fhir/StructureDefinition/implementationguide-page",
        "valueUri" : "CodeSystem-BRTipoObservacao.html"
      }],
      "reference" : {
        "reference" : "CodeSystem/BRTipoObservacao"
      },
      "name" : "Tipo de Observação (CodeSystem)",
      "description" : "Tipo de Observação."
    },
    {
      "extension" : [{
        "url" : "http://hl7.org/fhir/tools/StructureDefinition/resource-information",
        "valueString" : "CodeSystem"
      },
      {
        "url" : "http://hl7.org/fhir/StructureDefinition/implementationguide-page",
        "valueUri" : "CodeSystem-BRTurno.html"
      }],
      "reference" : {
        "reference" : "CodeSystem/BRTurno"
      },
      "name" : "Turno do dia (CodeSystem)",
      "description" : "Code System utilizado para definir o turno de um dia."
    },
    {
      "extension" : [{
        "url" : "http://hl7.org/fhir/tools/StructureDefinition/resource-information",
        "valueString" : "CodeSystem"
      },
      {
        "url" : "http://hl7.org/fhir/StructureDefinition/implementationguide-page",
        "valueUri" : "CodeSystem-BRUnidadeMedida.html"
      }],
      "reference" : {
        "reference" : "CodeSystem/BRUnidadeMedida"
      },
      "name" : "Unidade de Medida",
      "description" : "Code System utilizado para definir a unidade de medida de um medicamento prescrito, para consumo ou especificação do fabricante."
    },
    {
      "extension" : [{
        "url" : "http://hl7.org/fhir/tools/StructureDefinition/resource-information",
        "valueString" : "CodeSystem"
      },
      {
        "url" : "http://hl7.org/fhir/StructureDefinition/implementationguide-page",
        "valueUri" : "CodeSystem-BRUnidadeTempo.html"
      }],
      "reference" : {
        "reference" : "CodeSystem/BRUnidadeTempo"
      },
      "name" : "Unidade de tempo",
      "description" : "Code System utilizado para definir a classe de unidades de tempo."
    },
    {
      "extension" : [{
        "url" : "http://hl7.org/fhir/tools/StructureDefinition/resource-information",
        "valueString" : "CodeSystem"
      },
      {
        "url" : "http://hl7.org/fhir/StructureDefinition/implementationguide-page",
        "valueUri" : "CodeSystem-BRViaAdministracao.html"
      }],
      "reference" : {
        "reference" : "CodeSystem/BRViaAdministracao"
      },
      "name" : "Via de Administração",
      "description" : "Classifica a via na qual foi administrada uma substância em um indivíduo."
    },
    {
      "extension" : [{
        "url" : "http://hl7.org/fhir/tools/StructureDefinition/resource-information",
        "valueString" : "StructureDefinition:resource"
      },
      {
        "url" : "http://hl7.org/fhir/StructureDefinition/implementationguide-page",
        "valueUri" : "StructureDefinition-BRAlergiaReacaoAdversa-1.0.html"
      }],
      "reference" : {
        "reference" : "StructureDefinition/BRAlergiaReacaoAdversa-1.0"
      },
      "name" : "Alergia ou Reação Adversa",
      "description" : "Alergia ou Reação Adversa"
    },
    {
      "extension" : [{
        "url" : "http://hl7.org/fhir/tools/StructureDefinition/resource-information",
        "valueString" : "StructureDefinition:extension"
      },
      {
        "url" : "http://hl7.org/fhir/StructureDefinition/implementationguide-page",
        "valueUri" : "StructureDefinition-BRCodigoSerialMedicamento.html"
      }],
      "reference" : {
        "reference" : "StructureDefinition/BRCodigoSerialMedicamento"
      },
      "name" : "Código Serial de Medicamento",
      "description" : "Código Serial de Medicamento"
    },
    {
      "extension" : [{
        "url" : "http://hl7.org/fhir/tools/StructureDefinition/resource-information",
        "valueString" : "StructureDefinition:resource"
      },
      {
        "url" : "http://hl7.org/fhir/StructureDefinition/implementationguide-page",
        "valueUri" : "StructureDefinition-BRConjuntoMinimoDados-1.1.html"
      }],
      "reference" : {
        "reference" : "StructureDefinition/BRConjuntoMinimoDados-1.1"
      },
      "name" : "Conjunto Mínimo de Dados",
      "description" : "Documento público que coleta os dados dos atendimentos em saúde realizados em qualquer estabelecimento de saúde do país, público ou privado, em cada contato assistencial"
    },
    {
      "extension" : [{
        "url" : "http://hl7.org/fhir/tools/StructureDefinition/resource-information",
        "valueString" : "StructureDefinition:resource"
      },
      {
        "url" : "http://hl7.org/fhir/StructureDefinition/implementationguide-page",
        "valueUri" : "StructureDefinition-BRContatoAssistencial-1.0.html"
      }],
      "reference" : {
        "reference" : "StructureDefinition/BRContatoAssistencial-1.0"
      },
      "name" : "Contato Assistencial",
      "description" : "Resumo ou sumário referente a um atendimento ininterrupto dispensado a um indivíduo em uma mesma modalidade assistencial e em um mesmo estabelecimento de saúde, gerado após a conclusão deste atendimento."
    },
    {
      "extension" : [{
        "url" : "http://hl7.org/fhir/tools/StructureDefinition/resource-information",
        "valueString" : "StructureDefinition:extension"
      },
      {
        "url" : "http://hl7.org/fhir/StructureDefinition/implementationguide-page",
        "valueUri" : "StructureDefinition-BRFinanciamento-1.0.html"
      }],
      "reference" : {
        "reference" : "StructureDefinition/BRFinanciamento-1.0"
      },
      "name" : "Financiamento",
      "description" : "Extensão utilizada para identificar financiamento."
    },
    {
      "extension" : [{
        "url" : "http://hl7.org/fhir/tools/StructureDefinition/resource-information",
        "valueString" : "StructureDefinition:extension"
      },
      {
        "url" : "http://hl7.org/fhir/StructureDefinition/implementationguide-page",
        "valueUri" : "StructureDefinition-BRIdentificacaoEquipe-1.0.html"
      }],
      "reference" : {
        "reference" : "StructureDefinition/BRIdentificacaoEquipe-1.0"
      },
      "name" : "Identificador Nacional de Equipe",
      "description" : "Extensão para permitir informar o código do Identificador Nacional de Equipe."
    },
    {
      "extension" : [{
        "url" : "http://hl7.org/fhir/tools/StructureDefinition/resource-information",
        "valueString" : "StructureDefinition:extension"
      },
      {
        "url" : "http://hl7.org/fhir/StructureDefinition/implementationguide-page",
        "valueUri" : "StructureDefinition-BRIndividuoNaoIdentificado-1.0.html"
      }],
      "reference" : {
        "reference" : "StructureDefinition/BRIndividuoNaoIdentificado-1.0"
      },
      "name" : "Informações Complementares de Indivíduos Não Identificados",
      "description" : "Informações complementares necessárias ao Contato Assistencial na hipótese do indivíduo não poder ser identificado."
    },
    {
      "extension" : [{
        "url" : "http://hl7.org/fhir/tools/StructureDefinition/resource-information",
        "valueString" : "StructureDefinition:extension"
      },
      {
        "url" : "http://hl7.org/fhir/StructureDefinition/implementationguide-page",
        "valueUri" : "StructureDefinition-BRIntervaloDoses.html"
      }],
      "reference" : {
        "reference" : "StructureDefinition/BRIntervaloDoses"
      },
      "name" : "Intervalo de Doses",
      "description" : "Extensão para descrever uma unidade de tempo referenciada pelo UCUM."
    },
    {
      "extension" : [{
        "url" : "http://hl7.org/fhir/tools/StructureDefinition/resource-information",
        "valueString" : "StructureDefinition:resource"
      },
      {
        "url" : "http://hl7.org/fhir/StructureDefinition/implementationguide-page",
        "valueUri" : "StructureDefinition-BRLocalAtendimento-1.0.html"
      }],
      "reference" : {
        "reference" : "StructureDefinition/BRLocalAtendimento-1.0"
      },
      "name" : "Local de Atendimento",
      "description" : "Uma referência genérica aos locais onde um Contato Assistencial pode acontecer."
    },
    {
      "extension" : [{
        "url" : "http://hl7.org/fhir/tools/StructureDefinition/resource-information",
        "valueString" : "StructureDefinition:resource"
      },
      {
        "url" : "http://hl7.org/fhir/StructureDefinition/implementationguide-page",
        "valueUri" : "StructureDefinition-BRMedicamento.html"
      }],
      "reference" : {
        "reference" : "StructureDefinition/BRMedicamento"
      },
      "name" : "Medicamento (StructureDefinition)",
      "description" : "Medicamento"
    },
    {
      "extension" : [{
        "url" : "http://hl7.org/fhir/tools/StructureDefinition/resource-information",
        "valueString" : "StructureDefinition:resource"
      },
      {
        "url" : "http://hl7.org/fhir/StructureDefinition/implementationguide-page",
        "valueUri" : "StructureDefinition-BRObservacaoDescritiva-1.0.html"
      }],
      "reference" : {
        "reference" : "StructureDefinition/BRObservacaoDescritiva-1.0"
      },
      "name" : "Observação Descritiva",
      "description" : "Descrições textuais simples sobre um paciente."
    },
    {
      "extension" : [{
        "url" : "http://hl7.org/fhir/tools/StructureDefinition/resource-information",
        "valueString" : "StructureDefinition:extension"
      },
      {
        "url" : "http://hl7.org/fhir/StructureDefinition/implementationguide-page",
        "valueUri" : "StructureDefinition-BROcupacao-1.0.html"
      }],
      "reference" : {
        "reference" : "StructureDefinition/BROcupacao-1.0"
      },
      "name" : "Ocupação",
      "description" : "Extensão para incluir a Ocupação"
    },
    {
      "extension" : [{
        "url" : "http://hl7.org/fhir/tools/StructureDefinition/resource-information",
        "valueString" : "StructureDefinition:extension"
      },
      {
        "url" : "http://hl7.org/fhir/StructureDefinition/implementationguide-page",
        "valueUri" : "StructureDefinition-BROutrasInformacoes.html"
      }],
      "reference" : {
        "reference" : "StructureDefinition/BROutrasInformacoes"
      },
      "name" : "Outras Informações",
      "description" : "Representa quaisquer outras informações acerca dos dados de desfecho do atendimento registrado."
    },
    {
      "extension" : [{
        "url" : "http://hl7.org/fhir/tools/StructureDefinition/resource-information",
        "valueString" : "StructureDefinition:resource"
      },
      {
        "url" : "http://hl7.org/fhir/StructureDefinition/implementationguide-page",
        "valueUri" : "StructureDefinition-BRPlanoCuidados-1.0.html"
      }],
      "reference" : {
        "reference" : "StructureDefinition/BRPlanoCuidados-1.0"
      },
      "name" : "Plano de Cuidados",
      "description" : "Descreve o plano de cuidados, instruções e recomendações."
    },
    {
      "extension" : [{
        "url" : "http://hl7.org/fhir/tools/StructureDefinition/resource-information",
        "valueString" : "StructureDefinition:resource"
      },
      {
        "url" : "http://hl7.org/fhir/StructureDefinition/implementationguide-page",
        "valueUri" : "StructureDefinition-BRPrescricaoMedicamento.html"
      }],
      "reference" : {
        "reference" : "StructureDefinition/BRPrescricaoMedicamento"
      },
      "name" : "Prescrição de Medicamento",
      "description" : "Prescrição de Medicamento"
    },
    {
      "extension" : [{
        "url" : "http://hl7.org/fhir/tools/StructureDefinition/resource-information",
        "valueString" : "StructureDefinition:resource"
      },
      {
        "url" : "http://hl7.org/fhir/StructureDefinition/implementationguide-page",
        "valueUri" : "StructureDefinition-BRProblemaDiagnostico.html"
      }],
      "reference" : {
        "reference" : "StructureDefinition/BRProblemaDiagnostico"
      },
      "name" : "Problema / Diagnóstico",
      "description" : "Problema e/ou diagnóstico atribuído pelo profissional de saúde ao indivíduo no contato assistencial."
    },
    {
      "extension" : [{
        "url" : "http://hl7.org/fhir/tools/StructureDefinition/resource-information",
        "valueString" : "StructureDefinition:resource"
      },
      {
        "url" : "http://hl7.org/fhir/StructureDefinition/implementationguide-page",
        "valueUri" : "StructureDefinition-BRProcedimentoRealizado-1.0.html"
      }],
      "reference" : {
        "reference" : "StructureDefinition/BRProcedimentoRealizado-1.0"
      },
      "name" : "Procedimento Realizado",
      "description" : "Procedimento realizado em um indivíduo."
    },
    {
      "extension" : [{
        "url" : "http://hl7.org/fhir/tools/StructureDefinition/resource-information",
        "valueString" : "StructureDefinition:extension"
      },
      {
        "url" : "http://hl7.org/fhir/StructureDefinition/implementationguide-page",
        "valueUri" : "StructureDefinition-BRQuantidade-1.0.html"
      }],
      "reference" : {
        "reference" : "StructureDefinition/BRQuantidade-1.0"
      },
      "name" : "Quantidade",
      "description" : "Extensão para identificar quantidades."
    },
    {
      "extension" : [{
        "url" : "http://hl7.org/fhir/tools/StructureDefinition/resource-information",
        "valueString" : "StructureDefinition:resource"
      },
      {
        "url" : "http://hl7.org/fhir/StructureDefinition/implementationguide-page",
        "valueUri" : "StructureDefinition-BRRegistroPrescricaoMedicamento.html"
      }],
      "reference" : {
        "reference" : "StructureDefinition/BRRegistroPrescricaoMedicamento"
      },
      "name" : "Registro de Prescrição de Medicamento",
      "description" : "Modelo que gera o documento de Registro de Prescrição de Medicamento"
    },
    {
      "extension" : [{
        "url" : "http://hl7.org/fhir/tools/StructureDefinition/resource-information",
        "valueString" : "StructureDefinition:resource"
      },
      {
        "url" : "http://hl7.org/fhir/StructureDefinition/implementationguide-page",
        "valueUri" : "StructureDefinition-BRRestricaoFuncionalIncapacidadeSaude-1.0.html"
      }],
      "reference" : {
        "reference" : "StructureDefinition/BRRestricaoFuncionalIncapacidadeSaude-1.0"
      },
      "name" : "Restrições Funcionais e Incapacidades em Saúde",
      "description" : "Registra restrições funcionais ou incapacidades em saúde observadas no indivíduo."
    },
    {
      "extension" : [{
        "url" : "http://hl7.org/fhir/tools/StructureDefinition/resource-information",
        "valueString" : "StructureDefinition:resource"
      },
      {
        "url" : "http://hl7.org/fhir/StructureDefinition/implementationguide-page",
        "valueUri" : "StructureDefinition-BRResumoEvolucaoClinica.html"
      }],
      "reference" : {
        "reference" : "StructureDefinition/BRResumoEvolucaoClinica"
      },
      "name" : "Resumo da Evolução Clínica",
      "description" : "Descrição da evolução clínica do indivíduo."
    },
    {
      "extension" : [{
        "url" : "http://hl7.org/fhir/tools/StructureDefinition/resource-information",
        "valueString" : "StructureDefinition:resource"
      },
      {
        "url" : "http://hl7.org/fhir/StructureDefinition/implementationguide-page",
        "valueUri" : "StructureDefinition-BRSumarioAlta.html"
      }],
      "reference" : {
        "reference" : "StructureDefinition/BRSumarioAlta"
      },
      "name" : "Sumário de Alta (SA)",
      "description" : "O sumário de alta apresenta o conjunto dos principais registros realizados durante a permanência do indivíduo em um atendimento, como evolução clínica, procedimentos assistenciais, intervenções clínicas e diagnósticas, condutas adotadas e iniciadas para seguimento em clínica ou outro estabelecimento de assistência à saúde, e principalmente no final de sua permanência. A troca das informações essenciais referente ao período de permanência do indivíduo em um estabelecimento de saúde garante sua segurança na continuidade do tratamento. (Resolução CIT Nº 33, de 22 de março de 2018)"
    },
    {
      "extension" : [{
        "url" : "http://hl7.org/fhir/tools/StructureDefinition/resource-information",
        "valueString" : "StructureDefinition:extension"
      },
      {
        "url" : "http://hl7.org/fhir/StructureDefinition/implementationguide-page",
        "valueUri" : "StructureDefinition-BRTurno.html"
      }],
      "reference" : {
        "reference" : "StructureDefinition/BRTurno"
      },
      "name" : "Turno",
      "description" : "Extensão para descrever uma unidade de tempo referenciada pelo UCUM."
    },
    {
      "extension" : [{
        "url" : "http://hl7.org/fhir/tools/StructureDefinition/resource-information",
        "valueString" : "ValueSet"
      },
      {
        "url" : "http://hl7.org/fhir/StructureDefinition/implementationguide-page",
        "valueUri" : "ValueSet-BRAlergenos-1.0.html"
      }],
      "reference" : {
        "reference" : "ValueSet/BRAlergenos-1.0"
      },
      "name" : "Alérgenos",
      "description" : "Descreve o agente capaz de causar alergia ou reação adversa em seres humanos."
    },
    {
      "extension" : [{
        "url" : "http://hl7.org/fhir/tools/StructureDefinition/resource-information",
        "valueString" : "ValueSet"
      },
      {
        "url" : "http://hl7.org/fhir/StructureDefinition/implementationguide-page",
        "valueUri" : "ValueSet-BRCaraterAtendimento-1.0.html"
      }],
      "reference" : {
        "reference" : "ValueSet/BRCaraterAtendimento-1.0"
      },
      "name" : "Caráter de atendimento do Contato Assistencial",
      "description" : "ValueSet utilizado para classificar a prioridade de realização de um Contato Assistencial."
    },
    {
      "extension" : [{
        "url" : "http://hl7.org/fhir/tools/StructureDefinition/resource-information",
        "valueString" : "ValueSet"
      },
      {
        "url" : "http://hl7.org/fhir/StructureDefinition/implementationguide-page",
        "valueUri" : "ValueSet-BRCategoriaAgenteAlergiasReacoesAdversas-1.0.html"
      }],
      "reference" : {
        "reference" : "ValueSet/BRCategoriaAgenteAlergiasReacoesAdversas-1.0"
      },
      "name" : "Categoria do Agente da Alergia ou Reação Adversa",
      "description" : "Categoriza a substância responsável por causar uma alergia ou reação adversa."
    },
    {
      "extension" : [{
        "url" : "http://hl7.org/fhir/tools/StructureDefinition/resource-information",
        "valueString" : "ValueSet"
      },
      {
        "url" : "http://hl7.org/fhir/StructureDefinition/implementationguide-page",
        "valueUri" : "ValueSet-BRCategoriaCondicao.html"
      }],
      "reference" : {
        "reference" : "ValueSet/BRCategoriaCondicao"
      },
      "name" : "Classificação de uma condição",
      "description" : "Tradução para o português do brasil da classificação de uma condição"
    },
    {
      "extension" : [{
        "url" : "http://hl7.org/fhir/tools/StructureDefinition/resource-information",
        "valueString" : "ValueSet"
      },
      {
        "url" : "http://hl7.org/fhir/StructureDefinition/implementationguide-page",
        "valueUri" : "ValueSet-BRCriticidadeAlergiasReacoesAdversas-1.0.html"
      }],
      "reference" : {
        "reference" : "ValueSet/BRCriticidadeAlergiasReacoesAdversas-1.0"
      },
      "name" : "Criticidade de Alergias e Reações Adversas",
      "description" : "Indica o potencial de danos nos órgãos críticos do sistema ou consequência de ameaça à vida.."
    },
    {
      "extension" : [{
        "url" : "http://hl7.org/fhir/tools/StructureDefinition/resource-information",
        "valueString" : "ValueSet"
      },
      {
        "url" : "http://hl7.org/fhir/StructureDefinition/implementationguide-page",
        "valueUri" : "ValueSet-BREstadoContatoAssistencial-1.0.html"
      }],
      "reference" : {
        "reference" : "ValueSet/BREstadoContatoAssistencial-1.0"
      },
      "name" : "Estado do Contato Assistencial",
      "description" : "Classifica o estado de um Contato Assistencial."
    },
    {
      "extension" : [{
        "url" : "http://hl7.org/fhir/tools/StructureDefinition/resource-information",
        "valueString" : "ValueSet"
      },
      {
        "url" : "http://hl7.org/fhir/StructureDefinition/implementationguide-page",
        "valueUri" : "ValueSet-BREstadoDocumento-1.0.html"
      }],
      "reference" : {
        "reference" : "ValueSet/BREstadoDocumento-1.0"
      },
      "name" : "Estado do Documento",
      "description" : "Classifica o estado do documento que está sendo trafegado."
    },
    {
      "extension" : [{
        "url" : "http://hl7.org/fhir/tools/StructureDefinition/resource-information",
        "valueString" : "ValueSet"
      },
      {
        "url" : "http://hl7.org/fhir/StructureDefinition/implementationguide-page",
        "valueUri" : "ValueSet-BREstadoEvento-1.0.html"
      }],
      "reference" : {
        "reference" : "ValueSet/BREstadoEvento-1.0"
      },
      "name" : "Estado do Evento",
      "description" : "Identificação do estado de um evento."
    },
    {
      "extension" : [{
        "url" : "http://hl7.org/fhir/tools/StructureDefinition/resource-information",
        "valueString" : "ValueSet"
      },
      {
        "url" : "http://hl7.org/fhir/StructureDefinition/implementationguide-page",
        "valueUri" : "ValueSet-BREstadoObservacao-1.0.html"
      }],
      "reference" : {
        "reference" : "ValueSet/BREstadoObservacao-1.0"
      },
      "name" : "Estado da Observação",
      "description" : "Tipos de estados de uma observação."
    },
    {
      "extension" : [{
        "url" : "http://hl7.org/fhir/tools/StructureDefinition/resource-information",
        "valueString" : "ValueSet"
      },
      {
        "url" : "http://hl7.org/fhir/StructureDefinition/implementationguide-page",
        "valueUri" : "ValueSet-BREstadoResolucaoDiagnosticoProblema-1.0.html"
      }],
      "reference" : {
        "reference" : "ValueSet/BREstadoResolucaoDiagnosticoProblema-1.0"
      },
      "name" : "Estado da Resolução de Diagnóstico ou Problema",
      "description" : "Estado da resolução de um diagnóstico ou problema."
    },
    {
      "extension" : [{
        "url" : "http://hl7.org/fhir/tools/StructureDefinition/resource-information",
        "valueString" : "ValueSet"
      },
      {
        "url" : "http://hl7.org/fhir/StructureDefinition/implementationguide-page",
        "valueUri" : "ValueSet-BREstadoRestricaoFuncionalIncapacidadeSaude-1.0.html"
      }],
      "reference" : {
        "reference" : "ValueSet/BREstadoRestricaoFuncionalIncapacidadeSaude-1.0"
      },
      "name" : "Estado da Restrição Funcional ou Incapacidade de Saúde",
      "description" : "Estado da Restrição Funcional ou Incapacidade de Saúde"
    },
    {
      "extension" : [{
        "url" : "http://hl7.org/fhir/tools/StructureDefinition/resource-information",
        "valueString" : "ValueSet"
      },
      {
        "url" : "http://hl7.org/fhir/StructureDefinition/implementationguide-page",
        "valueUri" : "ValueSet-BREstadoSolicitacao-1.0.html"
      }],
      "reference" : {
        "reference" : "ValueSet/BREstadoSolicitacao-1.0"
      },
      "name" : "Estado da Solicitação",
      "description" : "Estado da solicitação."
    },
    {
      "extension" : [{
        "url" : "http://hl7.org/fhir/tools/StructureDefinition/resource-information",
        "valueString" : "ValueSet"
      },
      {
        "url" : "http://hl7.org/fhir/StructureDefinition/implementationguide-page",
        "valueUri" : "ValueSet-BREstadoSolicitacaoMedicamento-1.0.html"
      }],
      "reference" : {
        "reference" : "ValueSet/BREstadoSolicitacaoMedicamento-1.0"
      },
      "name" : "Estado da Solicitação de Medicamento",
      "description" : "Estado da Solicitação de Medicamento"
    },
    {
      "extension" : [{
        "url" : "http://hl7.org/fhir/tools/StructureDefinition/resource-information",
        "valueString" : "ValueSet"
      },
      {
        "url" : "http://hl7.org/fhir/StructureDefinition/implementationguide-page",
        "valueUri" : "ValueSet-BRFinanciamento-1.0.html"
      }],
      "reference" : {
        "reference" : "ValueSet/BRFinanciamento-1.0"
      },
      "name" : "Financiamento do procedimento realizado (ValueSet)",
      "description" : "Descreve o agente, instituição ou entidade responsável por custear as ações e serviços de saúde."
    },
    {
      "extension" : [{
        "url" : "http://hl7.org/fhir/tools/StructureDefinition/resource-information",
        "valueString" : "ValueSet"
      },
      {
        "url" : "http://hl7.org/fhir/StructureDefinition/implementationguide-page",
        "valueUri" : "ValueSet-BRGrauCertezaAlergiasReacoesAdversas-1.0.html"
      }],
      "reference" : {
        "reference" : "ValueSet/BRGrauCertezaAlergiasReacoesAdversas-1.0"
      },
      "name" : "Grau de Certeza de Alergias e Reações Adversas",
      "description" : "Indica o grau de certeza que se possui ao avaliar uma alergia ou reação adversa."
    },
    {
      "extension" : [{
        "url" : "http://hl7.org/fhir/tools/StructureDefinition/resource-information",
        "valueString" : "ValueSet"
      },
      {
        "url" : "http://hl7.org/fhir/StructureDefinition/implementationguide-page",
        "valueUri" : "ValueSet-BRJustificativaIndividuoNaoIdentificado-1.0.html"
      }],
      "reference" : {
        "reference" : "ValueSet/BRJustificativaIndividuoNaoIdentificado-1.0"
      },
      "name" : "Justificativa da Impossibilidade de Identificação do Indivíduo (ValueSet)",
      "description" : "Classifica as razões pelo qual não foi possível obter os dados de identificação do indivíduo em um contato assistencial. (Port. nº 84/SAS/MS/1997 e Port. nº02/SAS/SGEP/MS/2012)"
    },
    {
      "extension" : [{
        "url" : "http://hl7.org/fhir/tools/StructureDefinition/resource-information",
        "valueString" : "ValueSet"
      },
      {
        "url" : "http://hl7.org/fhir/StructureDefinition/implementationguide-page",
        "valueUri" : "ValueSet-BRModalidadeAssistencial-1.0.html"
      }],
      "reference" : {
        "reference" : "ValueSet/BRModalidadeAssistencial-1.0"
      },
      "name" : "Modalidade Assistencial (ValueSet)",
      "description" : "Classificação dos documentos e contatos assistenciais de acordo com as especificidades do modo, local e duração do atendimento."
    },
    {
      "extension" : [{
        "url" : "http://hl7.org/fhir/tools/StructureDefinition/resource-information",
        "valueString" : "ValueSet"
      },
      {
        "url" : "http://hl7.org/fhir/StructureDefinition/implementationguide-page",
        "valueUri" : "ValueSet-BRModalidadeTelessaude.html"
      }],
      "reference" : {
        "reference" : "ValueSet/BRModalidadeTelessaude"
      },
      "name" : "Modalidade de Telessaúde (ValueSet)",
      "description" : "Conjunto de códigos utilizados para identificar as modalidades de telessaúde no contexto do atendimento clínico."
    },
    {
      "extension" : [{
        "url" : "http://hl7.org/fhir/tools/StructureDefinition/resource-information",
        "valueString" : "ValueSet"
      },
      {
        "url" : "http://hl7.org/fhir/StructureDefinition/implementationguide-page",
        "valueUri" : "ValueSet-BRMotivoDesfecho-1.0.html"
      }],
      "reference" : {
        "reference" : "ValueSet/BRMotivoDesfecho-1.0"
      },
      "name" : "Motivo do desfecho do Contato assistencial",
      "description" : "ValueSet utilizado para classificar o motivo de conclusão total ou parcial do contato assistencial."
    },
    {
      "extension" : [{
        "url" : "http://hl7.org/fhir/tools/StructureDefinition/resource-information",
        "valueString" : "ValueSet"
      },
      {
        "url" : "http://hl7.org/fhir/StructureDefinition/implementationguide-page",
        "valueUri" : "ValueSet-BROcupacao-1.0.html"
      }],
      "reference" : {
        "reference" : "ValueSet/BROcupacao-1.0"
      },
      "name" : "Classificação Brasileira de Ocupações - CBO (ValueSet)",
      "description" : "Classifica as profissões do mercado de trabalho brasileiro."
    },
    {
      "extension" : [{
        "url" : "http://hl7.org/fhir/tools/StructureDefinition/resource-information",
        "valueString" : "ValueSet"
      },
      {
        "url" : "http://hl7.org/fhir/StructureDefinition/implementationguide-page",
        "valueUri" : "ValueSet-BRPapelProblemaDiagnostico.html"
      }],
      "reference" : {
        "reference" : "ValueSet/BRPapelProblemaDiagnostico"
      },
      "name" : "Classificação do papel de um problema e diagnóstico (ValueSet)",
      "description" : "Tradução para o português do brasil da classificação do papel de um problema/diagnóstico."
    },
    {
      "extension" : [{
        "url" : "http://hl7.org/fhir/tools/StructureDefinition/resource-information",
        "valueString" : "ValueSet"
      },
      {
        "url" : "http://hl7.org/fhir/StructureDefinition/implementationguide-page",
        "valueUri" : "ValueSet-BRPrescricaoNaoEstruturada.html"
      }],
      "reference" : {
        "reference" : "ValueSet/BRPrescricaoNaoEstruturada"
      },
      "name" : "Indicativo de prescrição não estruturada ou medicamento não identificado",
      "description" : "Indicativo de prescrição não estruturada ou medicamento não identificado."
    },
    {
      "extension" : [{
        "url" : "http://hl7.org/fhir/tools/StructureDefinition/resource-information",
        "valueString" : "ValueSet"
      },
      {
        "url" : "http://hl7.org/fhir/StructureDefinition/implementationguide-page",
        "valueUri" : "ValueSet-BRProblemaDiagnostico.html"
      }],
      "reference" : {
        "reference" : "ValueSet/BRProblemaDiagnostico"
      },
      "name" : "Classificação Internacional de Doenças e Atenção Primária",
      "description" : "Código Internacional de Atenção Primária (CIAP2) e Classificação Internacional de Doenças (CID10)"
    },
    {
      "extension" : [{
        "url" : "http://hl7.org/fhir/tools/StructureDefinition/resource-information",
        "valueString" : "ValueSet"
      },
      {
        "url" : "http://hl7.org/fhir/StructureDefinition/implementationguide-page",
        "valueUri" : "ValueSet-BRProcedencia-1.0.html"
      }],
      "reference" : {
        "reference" : "ValueSet/BRProcedencia-1.0"
      },
      "name" : "Procedência do Contato Assistencial",
      "description" : "Classifica o serviço que encaminhou o indivíduo ou a sua iniciativa/de seu responsável na busca pelo acesso ao serviço de saúde."
    },
    {
      "extension" : [{
        "url" : "http://hl7.org/fhir/tools/StructureDefinition/resource-information",
        "valueString" : "ValueSet"
      },
      {
        "url" : "http://hl7.org/fhir/StructureDefinition/implementationguide-page",
        "valueUri" : "ValueSet-BRProcedimentosNacionais-1.0.html"
      }],
      "reference" : {
        "reference" : "ValueSet/BRProcedimentosNacionais-1.0"
      },
      "name" : "Procedimento realizado",
      "description" : "ValueSet das classificações brasileiras para procedimentos adotadas em contexto nacional, os CodeSystems apresentam os códigos da competência atual, para o envio de competência anterior os códigos devem ser consultados na RTS."
    },
    {
      "extension" : [{
        "url" : "http://hl7.org/fhir/tools/StructureDefinition/resource-information",
        "valueString" : "ValueSet"
      },
      {
        "url" : "http://hl7.org/fhir/StructureDefinition/implementationguide-page",
        "valueUri" : "ValueSet-BRReacoesAdversasMedDRA-1.0.html"
      }],
      "reference" : {
        "reference" : "ValueSet/BRReacoesAdversasMedDRA-1.0"
      },
      "name" : "Reações Adversas da MedDRA",
      "description" : "Classifica as reações adversas de acordo com o Medical Dictionary for Regulatory Activities."
    },
    {
      "extension" : [{
        "url" : "http://hl7.org/fhir/tools/StructureDefinition/resource-information",
        "valueString" : "ValueSet"
      },
      {
        "url" : "http://hl7.org/fhir/StructureDefinition/implementationguide-page",
        "valueUri" : "ValueSet-BRResponsabilidadeParticipante-1.0.html"
      }],
      "reference" : {
        "reference" : "ValueSet/BRResponsabilidadeParticipante-1.0"
      },
      "name" : "Reponsabilidade no Contato Assistencial",
      "description" : "Classifica o tipo de responsabilidade de indivíduos ou profissionais no Contato Assistencial."
    },
    {
      "extension" : [{
        "url" : "http://hl7.org/fhir/tools/StructureDefinition/resource-information",
        "valueString" : "ValueSet"
      },
      {
        "url" : "http://hl7.org/fhir/StructureDefinition/implementationguide-page",
        "valueUri" : "ValueSet-BRSexo-1.0.html"
      }],
      "reference" : {
        "reference" : "ValueSet/BRSexo-1.0"
      },
      "name" : "Sexo",
      "description" : "Sexo de um indivíduo."
    },
    {
      "extension" : [{
        "url" : "http://hl7.org/fhir/tools/StructureDefinition/resource-information",
        "valueString" : "ValueSet"
      },
      {
        "url" : "http://hl7.org/fhir/StructureDefinition/implementationguide-page",
        "valueUri" : "ValueSet-BRTerminologiaMedicamento.html"
      }],
      "reference" : {
        "reference" : "ValueSet/BRTerminologiaMedicamento"
      },
      "name" : "Terminologia dos medicamentos",
      "description" : "ValueSet utilizado para definir a terminologia de um dado medicamento."
    },
    {
      "extension" : [{
        "url" : "http://hl7.org/fhir/tools/StructureDefinition/resource-information",
        "valueString" : "ValueSet"
      },
      {
        "url" : "http://hl7.org/fhir/StructureDefinition/implementationguide-page",
        "valueUri" : "ValueSet-BRTipoDocumento-1.0.html"
      }],
      "reference" : {
        "reference" : "ValueSet/BRTipoDocumento-1.0"
      },
      "name" : "Tipo de Documento (ValueSet)",
      "description" : "Classifica o tipo de documento que está sendo trafegado."
    },
    {
      "extension" : [{
        "url" : "http://hl7.org/fhir/tools/StructureDefinition/resource-information",
        "valueString" : "ValueSet"
      },
      {
        "url" : "http://hl7.org/fhir/StructureDefinition/implementationguide-page",
        "valueUri" : "ValueSet-BRTipoIdentificadorProcedimento-1.0.html"
      }],
      "reference" : {
        "reference" : "ValueSet/BRTipoIdentificadorProcedimento-1.0"
      },
      "name" : "Tipo de Identificador do Procedimento",
      "description" : "Classifica o tipo de identificador que está sendo utilizado para o procedimento."
    },
    {
      "extension" : [{
        "url" : "http://hl7.org/fhir/tools/StructureDefinition/resource-information",
        "valueString" : "ValueSet"
      },
      {
        "url" : "http://hl7.org/fhir/StructureDefinition/implementationguide-page",
        "valueUri" : "ValueSet-BRTipoObservacao-1.0.html"
      }],
      "reference" : {
        "reference" : "ValueSet/BRTipoObservacao-1.0"
      },
      "name" : "Tipo de Observação (ValueSet)",
      "description" : "Tipo de Observação."
    },
    {
      "extension" : [{
        "url" : "http://hl7.org/fhir/tools/StructureDefinition/resource-information",
        "valueString" : "ValueSet"
      },
      {
        "url" : "http://hl7.org/fhir/StructureDefinition/implementationguide-page",
        "valueUri" : "ValueSet-BRTurno.html"
      }],
      "reference" : {
        "reference" : "ValueSet/BRTurno"
      },
      "name" : "Turno do dia (ValueSet)",
      "description" : "ValueSet utilizado para definir o turno de um dia."
    },
    {
      "extension" : [{
        "url" : "http://hl7.org/fhir/tools/StructureDefinition/resource-information",
        "valueString" : "ValueSet"
      },
      {
        "url" : "http://hl7.org/fhir/StructureDefinition/implementationguide-page",
        "valueUri" : "ValueSet-BRUnidadeConsumo.html"
      }],
      "reference" : {
        "reference" : "ValueSet/BRUnidadeConsumo"
      },
      "name" : "Unidade de Consumo",
      "description" : "ValueSet utilizado para definir a unidade de consumo de um medicamento prescrito."
    },
    {
      "extension" : [{
        "url" : "http://hl7.org/fhir/tools/StructureDefinition/resource-information",
        "valueString" : "ValueSet"
      },
      {
        "url" : "http://hl7.org/fhir/StructureDefinition/implementationguide-page",
        "valueUri" : "ValueSet-BRUnidadeMedidaMedicamento.html"
      }],
      "reference" : {
        "reference" : "ValueSet/BRUnidadeMedidaMedicamento"
      },
      "name" : "Unidade de Medida de Medicamento",
      "description" : "ValueSet utilizado para definir a unidade de medida de medicamentos sob informações do fabricante."
    },
    {
      "extension" : [{
        "url" : "http://hl7.org/fhir/tools/StructureDefinition/resource-information",
        "valueString" : "ValueSet"
      },
      {
        "url" : "http://hl7.org/fhir/StructureDefinition/implementationguide-page",
        "valueUri" : "ValueSet-BRUnidadeTempo.html"
      }],
      "reference" : {
        "reference" : "ValueSet/BRUnidadeTempo"
      },
      "name" : "Unidade de Tempo",
      "description" : "ValueSet utilizado para definir uma unidade de tempo."
    },
    {
      "extension" : [{
        "url" : "http://hl7.org/fhir/tools/StructureDefinition/resource-information",
        "valueString" : "ValueSet"
      },
      {
        "url" : "http://hl7.org/fhir/StructureDefinition/implementationguide-page",
        "valueUri" : "ValueSet-BRViaAdministracao-1.0.html"
      }],
      "reference" : {
        "reference" : "ValueSet/BRViaAdministracao-1.0"
      },
      "name" : "Via de Administração do Imunobiológico",
      "description" : "Via de administração de um imunobiológico."
    }],
    "page" : {
      "extension" : [{
        "url" : "http://hl7.org/fhir/StructureDefinition/structuredefinition-standards-status",
        "valueCode" : "informative"
      },
      {
        "url" : "http://hl7.org/fhir/tools/StructureDefinition/ig-page-name",
        "valueUrl" : "toc.html"
      }],
      "nameUrl" : "toc.html",
      "title" : "Índice",
      "generation" : "html",
      "page" : [{
        "extension" : [{
          "url" : "http://hl7.org/fhir/StructureDefinition/structuredefinition-standards-status",
          "valueCode" : "informative"
        },
        {
          "url" : "http://hl7.org/fhir/tools/StructureDefinition/ig-page-name",
          "valueUrl" : "index.html"
        }],
        "nameUrl" : "index.html",
        "title" : "Principal",
        "generation" : "html"
      },
      {
        "extension" : [{
          "url" : "http://hl7.org/fhir/StructureDefinition/structuredefinition-standards-status",
          "valueCode" : "informative"
        },
        {
          "url" : "http://hl7.org/fhir/tools/StructureDefinition/ig-page-name",
          "valueUrl" : "credenciamento.html"
        }],
        "nameUrl" : "credenciamento.html",
        "title" : "Credenciamento",
        "generation" : "html"
      },
      {
        "extension" : [{
          "url" : "http://hl7.org/fhir/StructureDefinition/structuredefinition-standards-status",
          "valueCode" : "informative"
        },
        {
          "url" : "http://hl7.org/fhir/tools/StructureDefinition/ig-page-name",
          "valueUrl" : "integracao.html"
        }],
        "nameUrl" : "integracao.html",
        "title" : "Integração",
        "generation" : "html"
      },
      {
        "extension" : [{
          "url" : "http://hl7.org/fhir/StructureDefinition/structuredefinition-standards-status",
          "valueCode" : "informative"
        },
        {
          "url" : "http://hl7.org/fhir/tools/StructureDefinition/ig-page-name",
          "valueUrl" : "miSA.html"
        }],
        "nameUrl" : "miSA.html",
        "title" : "Modelo de Informação",
        "generation" : "html"
      },
      {
        "extension" : [{
          "url" : "http://hl7.org/fhir/StructureDefinition/structuredefinition-standards-status",
          "valueCode" : "informative"
        },
        {
          "url" : "http://hl7.org/fhir/tools/StructureDefinition/ig-page-name",
          "valueUrl" : "mcSA.html"
        }],
        "nameUrl" : "mcSA.html",
        "title" : "Modelo Computacional",
        "generation" : "html"
      },
      {
        "extension" : [{
          "url" : "http://hl7.org/fhir/StructureDefinition/structuredefinition-standards-status",
          "valueCode" : "informative"
        },
        {
          "url" : "http://hl7.org/fhir/tools/StructureDefinition/ig-page-name",
          "valueUrl" : "exemplos.html"
        }],
        "nameUrl" : "exemplos.html",
        "title" : "Exemplos",
        "generation" : "html"
      },
      {
        "extension" : [{
          "url" : "http://hl7.org/fhir/StructureDefinition/structuredefinition-standards-status",
          "valueCode" : "informative"
        },
        {
          "url" : "http://hl7.org/fhir/tools/StructureDefinition/ig-page-name",
          "valueUrl" : "changes.html"
        }],
        "nameUrl" : "changes.html",
        "title" : "Histórico de mudanças",
        "generation" : "html"
      },
      {
        "extension" : [{
          "url" : "http://hl7.org/fhir/StructureDefinition/structuredefinition-standards-status",
          "valueCode" : "informative"
        },
        {
          "url" : "http://hl7.org/fhir/tools/StructureDefinition/ig-page-name",
          "valueUrl" : "downloads.html"
        }],
        "nameUrl" : "downloads.html",
        "title" : "Downloads",
        "generation" : "html"
      },
      {
        "extension" : [{
          "url" : "http://hl7.org/fhir/StructureDefinition/structuredefinition-standards-status",
          "valueCode" : "informative"
        },
        {
          "url" : "http://hl7.org/fhir/tools/StructureDefinition/ig-page-name",
          "valueUrl" : "forms.html"
        }],
        "nameUrl" : "forms.html",
        "title" : "Feedback",
        "generation" : "html"
      },
      {
        "extension" : [{
          "url" : "http://hl7.org/fhir/StructureDefinition/structuredefinition-standards-status",
          "valueCode" : "informative"
        },
        {
          "url" : "http://hl7.org/fhir/tools/StructureDefinition/ig-page-name",
          "valueUrl" : "suporte.html"
        }],
        "nameUrl" : "suporte.html",
        "title" : "Suporte da RNDS",
        "generation" : "html"
      }]
    },
    "parameter" : [{
      "code" : "path-resource",
      "value" : "input\\history"
    },
    {
      "code" : "path-resource",
      "value" : "input/resources"
    },
    {
      "code" : "path-pages",
      "value" : "input/pagecontent"
    },
    {
      "code" : "path-resource",
      "value" : "input/capabilities"
    },
    {
      "code" : "path-resource",
      "value" : "input/examples"
    },
    {
      "code" : "path-resource",
      "value" : "input/extensions"
    },
    {
      "code" : "path-resource",
      "value" : "input/models"
    },
    {
      "code" : "path-resource",
      "value" : "input/operations"
    },
    {
      "code" : "path-resource",
      "value" : "input/profiles"
    },
    {
      "code" : "path-resource",
      "value" : "input/vocabulary"
    },
    {
      "code" : "path-resource",
      "value" : "input/testing"
    },
    {
      "code" : "path-resource",
      "value" : "input/history"
    },
    {
      "code" : "path-resource",
      "value" : "fsh-generated/resources"
    },
    {
      "code" : "path-pages",
      "value" : "template/config"
    },
    {
      "code" : "path-pages",
      "value" : "input/assets"
    },
    {
      "code" : "path-pages",
      "value" : "input/images"
    },
    {
      "code" : "path-tx-cache",
      "value" : "input-cache/txcache"
    }]
  }
}

```
