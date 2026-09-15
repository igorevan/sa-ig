# Dose de Vacina - Guia de Implementação do Sumário de Alta (SA) da RNDS v1.0.0-release

## CodeSystem: Dose de Vacina 

 
Define a dose da administração de uma substância. 

This Code system is referenced in the definition of the following value sets:

* [Dose do Imunobiológico](ValueSet-BRDose-1.0.md)

-------

 [Description of the above table(s)](http://build.fhir.org/ig/FHIR/ig-guidance/readingIgs.html#terminology). 



## Resource Content

```json
{
  "resourceType" : "CodeSystem",
  "id" : "BRDose",
  "language" : "pt-BR",
  "extension" : [{
    "url" : "http://hl7.org/fhir/StructureDefinition/structuredefinition-wg",
    "valueCode" : "ehr"
  },
  {
    "url" : "http://hl7.org/fhir/StructureDefinition/structuredefinition-fmm",
    "valueInteger" : 1,
    "_valueInteger" : {
      "extension" : [{
        "url" : "http://hl7.org/fhir/StructureDefinition/structuredefinition-conformance-derivedFrom",
        "valueCanonical" : "https://fhir.saude.gov.br/sa/ImplementationGuide/br.gov.saude.sa.fhir"
      }]
    }
  },
  {
    "url" : "http://hl7.org/fhir/StructureDefinition/structuredefinition-standards-status",
    "valueCode" : "normative",
    "_valueCode" : {
      "extension" : [{
        "url" : "http://hl7.org/fhir/StructureDefinition/structuredefinition-conformance-derivedFrom",
        "valueCanonical" : "https://fhir.saude.gov.br/sa/ImplementationGuide/br.gov.saude.sa.fhir"
      }]
    }
  },
  {
    "url" : "http://hl7.org/fhir/StructureDefinition/structuredefinition-normative-version",
    "valueCode" : "4.0.1"
  }],
  "url" : "http://www.saude.gov.br/fhir/r4/CodeSystem/BRDose",
  "version" : "1.0.0-release",
  "name" : "BRDose",
  "title" : "Dose de Vacina",
  "status" : "active",
  "experimental" : false,
  "date" : "2020-01-06T18:23:38.3705+00:00",
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
  "description" : "Define a dose da administração de uma substância.",
  "jurisdiction" : [{
    "coding" : [{
      "system" : "urn:iso:std:iso:3166",
      "code" : "BR"
    }]
  }],
  "caseSensitive" : true,
  "content" : "complete",
  "concept" : [{
    "code" : "1",
    "display" : "1ª Dose",
    "definition" : "D1",
    "designation" : [{
      "language" : "en",
      "value" : "First dose"
    },
    {
      "language" : "es",
      "value" : "Primera dosis"
    }]
  },
  {
    "code" : "2",
    "display" : "2ª Dose",
    "definition" : "D2",
    "designation" : [{
      "language" : "en",
      "value" : "Second dose"
    },
    {
      "language" : "es",
      "value" : "Segunda dosis"
    }]
  },
  {
    "code" : "3",
    "display" : "3ª Dose",
    "definition" : "D3",
    "designation" : [{
      "language" : "en",
      "value" : "Third dose"
    },
    {
      "language" : "es",
      "value" : "Tercera dosis"
    }]
  },
  {
    "code" : "4",
    "display" : "4ª Dose",
    "definition" : "D4",
    "designation" : [{
      "language" : "en",
      "value" : "Fourth dose"
    },
    {
      "language" : "es",
      "value" : "Cuarta dosis"
    }]
  },
  {
    "code" : "5",
    "display" : "5ª Dose",
    "definition" : "D5",
    "designation" : [{
      "language" : "en",
      "value" : "Fifth dose"
    },
    {
      "language" : "es",
      "value" : "Quinta dosis"
    }]
  },
  {
    "code" : "6",
    "display" : "1º Reforço",
    "definition" : "R1",
    "designation" : [{
      "language" : "en",
      "value" : "First booster dose"
    },
    {
      "language" : "es",
      "value" : "Primer refuerzo"
    }]
  },
  {
    "code" : "7",
    "display" : "2º Reforço",
    "definition" : "R2",
    "designation" : [{
      "language" : "en",
      "value" : "Second booster dose"
    },
    {
      "language" : "es",
      "value" : "Segundo refuerzo"
    }]
  },
  {
    "code" : "8",
    "display" : "Dose",
    "definition" : "D",
    "designation" : [{
      "language" : "en",
      "value" : "Dose"
    },
    {
      "language" : "es",
      "value" : "Dosis"
    }]
  },
  {
    "code" : "9",
    "display" : "Única",
    "definition" : "DU",
    "designation" : [{
      "language" : "en",
      "value" : "Single dose"
    },
    {
      "language" : "es",
      "value" : "Dosis única"
    }]
  },
  {
    "code" : "10",
    "display" : "Revacinação",
    "definition" : "REV",
    "designation" : [{
      "language" : "en",
      "value" : "Revaccination"
    },
    {
      "language" : "es",
      "value" : "Revacunación"
    }]
  },
  {
    "code" : "11",
    "display" : "Tratamento com uma dose",
    "definition" : "T1",
    "designation" : [{
      "language" : "en",
      "value" : "1 dose treatment"
    },
    {
      "language" : "es",
      "value" : "Tratamiento de 1 dosis"
    }]
  },
  {
    "code" : "12",
    "display" : "Tratamento com duas doses",
    "definition" : "T2",
    "designation" : [{
      "language" : "en",
      "value" : "2 dose treatment"
    },
    {
      "language" : "es",
      "value" : "Tratamiento de 2 dosis"
    }]
  },
  {
    "code" : "13",
    "display" : "Tratamento com três doses",
    "definition" : "T3",
    "designation" : [{
      "language" : "en",
      "value" : "3 dose treatment"
    },
    {
      "language" : "es",
      "value" : "Tratamiento de 3 dosis"
    }]
  },
  {
    "code" : "14",
    "display" : "Tratamento com quatro doses",
    "definition" : "T4",
    "designation" : [{
      "language" : "en",
      "value" : "4 dose treatment"
    },
    {
      "language" : "es",
      "value" : "Tratamiento de 4 dosis"
    }]
  },
  {
    "code" : "15",
    "display" : "Tratamento com cinco doses",
    "definition" : "T5",
    "designation" : [{
      "language" : "en",
      "value" : "5 dose treatment"
    },
    {
      "language" : "es",
      "value" : "Tratamiento de 5 dosis"
    }]
  },
  {
    "code" : "16",
    "display" : "Tratamento com seis doses",
    "definition" : "T6",
    "designation" : [{
      "language" : "en",
      "value" : "6 dose treatment"
    },
    {
      "language" : "es",
      "value" : "Tratamiento de 6 dosis"
    }]
  },
  {
    "code" : "17",
    "display" : "Tratamento com sete doses",
    "definition" : "T7",
    "designation" : [{
      "language" : "en",
      "value" : "7 dose treatment"
    },
    {
      "language" : "es",
      "value" : "Tratamiento de 7 dosis"
    }]
  },
  {
    "code" : "18",
    "display" : "Tratamento com oito doses",
    "definition" : "T8",
    "designation" : [{
      "language" : "en",
      "value" : "8 dose treatment"
    },
    {
      "language" : "es",
      "value" : "Tratamiento de 8 dosis"
    }]
  },
  {
    "code" : "19",
    "display" : "Tratamento com nove doses",
    "definition" : "T9",
    "designation" : [{
      "language" : "en",
      "value" : "9 dose treatment"
    },
    {
      "language" : "es",
      "value" : "Tratamiento de 9 dosis"
    }]
  },
  {
    "code" : "20",
    "display" : "Tratamento com dez doses",
    "definition" : "T10",
    "designation" : [{
      "language" : "en",
      "value" : "10 dose treatment"
    },
    {
      "language" : "es",
      "value" : "Tratamiento de 10 dosis"
    }]
  },
  {
    "code" : "21",
    "display" : "Tratamento com onze doses",
    "definition" : "T11",
    "designation" : [{
      "language" : "en",
      "value" : "11 dose treatment"
    },
    {
      "language" : "es",
      "value" : "Tratamiento de 11 dosis"
    }]
  },
  {
    "code" : "22",
    "display" : "Tratamento com doze doses",
    "definition" : "T12",
    "designation" : [{
      "language" : "en",
      "value" : "12 dose treatment"
    },
    {
      "language" : "es",
      "value" : "Tratamiento de 12 dosis"
    }]
  },
  {
    "code" : "23",
    "display" : "Tratamento com treze doses",
    "definition" : "T13",
    "designation" : [{
      "language" : "en",
      "value" : "13 dose treatment"
    },
    {
      "language" : "es",
      "value" : "Tratamiento de 13 dosis"
    }]
  },
  {
    "code" : "24",
    "display" : "Tratamento com quartorze doses",
    "definition" : "T14",
    "designation" : [{
      "language" : "en",
      "value" : "14 dose treatment"
    },
    {
      "language" : "es",
      "value" : "Tratamiento de 14 dosis"
    }]
  },
  {
    "code" : "25",
    "display" : "Tratamento com quinze doses",
    "definition" : "T15",
    "designation" : [{
      "language" : "en",
      "value" : "15 dose treatment"
    },
    {
      "language" : "es",
      "value" : "Tratamiento de 15 dosis"
    }]
  },
  {
    "code" : "26",
    "display" : "Tratamento com dezesseis doses",
    "definition" : "T16",
    "designation" : [{
      "language" : "en",
      "value" : "16 dose treatment"
    },
    {
      "language" : "es",
      "value" : "Tratamiento de 16 dosis"
    }]
  },
  {
    "code" : "27",
    "display" : "Tratamento com dezessete doses",
    "definition" : "T17",
    "designation" : [{
      "language" : "en",
      "value" : "17 dose treatment"
    },
    {
      "language" : "es",
      "value" : "Tratamiento de 17 dosis"
    }]
  },
  {
    "code" : "28",
    "display" : "Tratamento com dezoito doses",
    "definition" : "T18",
    "designation" : [{
      "language" : "en",
      "value" : "18 dose treatment"
    },
    {
      "language" : "es",
      "value" : "Tratamiento de 18 dosis"
    }]
  },
  {
    "code" : "29",
    "display" : "Tratamento com dezenove doses",
    "definition" : "T19",
    "designation" : [{
      "language" : "en",
      "value" : "19 dose treatment"
    },
    {
      "language" : "es",
      "value" : "Tratamiento de 19 dosis"
    }]
  },
  {
    "code" : "30",
    "display" : "Tratamento com vinte doses",
    "definition" : "T20",
    "designation" : [{
      "language" : "en",
      "value" : "20 dose treatment"
    },
    {
      "language" : "es",
      "value" : "Tratamiento de 20 dosis"
    }]
  },
  {
    "code" : "31",
    "display" : "Tratamento com vinte e quatro doses",
    "definition" : "T24",
    "designation" : [{
      "language" : "en",
      "value" : "24 dose treatment"
    },
    {
      "language" : "es",
      "value" : "Tratamiento de 24 dosis"
    }]
  },
  {
    "code" : "32",
    "display" : "1ª Dose Revacinação",
    "definition" : "D1REV",
    "designation" : [{
      "language" : "en",
      "value" : "First dose revaccinacion"
    },
    {
      "language" : "es",
      "value" : "Primera dosis revacunación"
    }]
  },
  {
    "code" : "33",
    "display" : "2ª Dose Revacinação",
    "definition" : "D2REV",
    "designation" : [{
      "language" : "en",
      "value" : "Second dose revaccinacion"
    },
    {
      "language" : "es",
      "value" : "Segunda dosis revacunación"
    }]
  },
  {
    "code" : "34",
    "display" : "3ª Dose Revacinação",
    "definition" : "D3REV",
    "designation" : [{
      "language" : "en",
      "value" : "Third dose revaccinacion"
    },
    {
      "language" : "es",
      "value" : "Tecera dosis revacunación"
    }]
  },
  {
    "code" : "35",
    "display" : "4ª Dose Revacinação",
    "definition" : "D4REV",
    "designation" : [{
      "language" : "en",
      "value" : "Fourth dose revaccinacion"
    },
    {
      "language" : "es",
      "value" : "Cuarta dosis revacunación"
    }]
  },
  {
    "code" : "36",
    "display" : "Dose Inicial",
    "definition" : "DI",
    "designation" : [{
      "language" : "en",
      "value" : "Initial dose"
    },
    {
      "language" : "es",
      "value" : "Dosis inicial"
    }]
  },
  {
    "code" : "37",
    "display" : "Dose Adicional",
    "definition" : "DA",
    "designation" : [{
      "language" : "en",
      "value" : "Additional dose"
    },
    {
      "language" : "es",
      "value" : "Dosis adicional"
    }]
  },
  {
    "code" : "38",
    "display" : "Reforço",
    "definition" : "REF",
    "designation" : [{
      "language" : "en",
      "value" : "Booster"
    },
    {
      "language" : "es",
      "value" : "Refuerzo"
    }]
  },
  {
    "code" : "39",
    "display" : "3º Reforço",
    "definition" : "R3",
    "designation" : [{
      "language" : "en",
      "value" : "Third booster dose"
    },
    {
      "language" : "es",
      "value" : "Tercer refuerzo"
    }]
  },
  {
    "code" : "40",
    "display" : "4º Reforço",
    "definition" : "R4",
    "designation" : [{
      "language" : "en",
      "value" : "Fourth booster dose"
    },
    {
      "language" : "es",
      "value" : "Cuarto refuerzo"
    }]
  },
  {
    "code" : "41",
    "display" : "5º Reforço",
    "definition" : "R5",
    "designation" : [{
      "language" : "en",
      "value" : "Fifth booster dose"
    },
    {
      "language" : "es",
      "value" : "Quinto refuerzo"
    }]
  },
  {
    "code" : "42",
    "display" : "6º Reforço",
    "definition" : "R6",
    "designation" : [{
      "language" : "en",
      "value" : "Sixth booster dose"
    },
    {
      "language" : "es",
      "value" : "Sexto refuerzo"
    }]
  },
  {
    "code" : "43",
    "display" : "5ª Dose Revacinação",
    "definition" : "D5REV",
    "designation" : [{
      "language" : "en",
      "value" : "Fifth dose revaccinacion"
    },
    {
      "language" : "es",
      "value" : "Quinta dosis revacunación"
    }]
  },
  {
    "code" : "44",
    "display" : "1ª Dose Fracionada",
    "definition" : "D1F",
    "designation" : [{
      "language" : "en",
      "value" : "First fractional dose"
    },
    {
      "language" : "es",
      "value" : "Primera dosis fraccionada"
    }]
  },
  {
    "code" : "45",
    "display" : "2ª Dose Fracionada",
    "definition" : "D2F",
    "designation" : [{
      "language" : "en",
      "value" : "Second fractional dose"
    },
    {
      "language" : "es",
      "value" : "Secunda dosis fraccionada"
    }]
  },
  {
    "code" : "46",
    "display" : "3ª Dose Fracionada",
    "definition" : "D3F",
    "designation" : [{
      "language" : "en",
      "value" : "Third fractional dose"
    },
    {
      "language" : "es",
      "value" : "Tercera dosis fraccionada"
    }]
  },
  {
    "code" : "47",
    "display" : "4ª Dose Fracionada",
    "definition" : "D4F",
    "designation" : [{
      "language" : "en",
      "value" : "Fourth fractional dose"
    },
    {
      "language" : "es",
      "value" : "Cuarta dosis fraccionada"
    }]
  },
  {
    "code" : "48",
    "display" : "5ª Dose Fracionada",
    "definition" : "D5F",
    "designation" : [{
      "language" : "en",
      "value" : "Fifth fractional dose"
    },
    {
      "language" : "es",
      "value" : "Quinta dosis fraccionada"
    }]
  },
  {
    "code" : "49",
    "display" : "1ª Dose Dobrada",
    "definition" : "D1D",
    "designation" : [{
      "language" : "en",
      "value" : "1st double dose"
    },
    {
      "language" : "es",
      "value" : "1ra dosis doble"
    }]
  },
  {
    "code" : "50",
    "display" : "2ª Dose Dobrada",
    "definition" : "D2D",
    "designation" : [{
      "language" : "en",
      "value" : "2nd double dose"
    },
    {
      "language" : "es",
      "value" : "2da dosis doble"
    }]
  },
  {
    "code" : "51",
    "display" : "3ª Dose Dobrada",
    "definition" : "D3D",
    "designation" : [{
      "language" : "en",
      "value" : "3rd double dose"
    },
    {
      "language" : "es",
      "value" : "3ra dosis doble"
    }]
  },
  {
    "code" : "52",
    "display" : "4ª Dose Dobrada",
    "definition" : "D4D",
    "designation" : [{
      "language" : "en",
      "value" : "4th double dose"
    },
    {
      "language" : "es",
      "value" : "4ta dosis doble"
    }]
  },
  {
    "code" : "53",
    "display" : "1ª Dose Revacinação Dobrada",
    "definition" : "D1REVD"
  },
  {
    "code" : "54",
    "display" : "2ª Dose Revacinação Dobrada",
    "definition" : "D2REVD"
  },
  {
    "code" : "55",
    "display" : "3ª Dose Revacinação Dobrada",
    "definition" : "D3REVD"
  },
  {
    "code" : "56",
    "display" : "4ª Dose Revacinação Dobrada",
    "definition" : "D4REVD"
  },
  {
    "code" : "57",
    "display" : "Dose Zero",
    "definition" : "D0",
    "designation" : [{
      "language" : "en",
      "value" : "Zero-dose"
    },
    {
      "language" : "es",
      "value" : "Dosis cero"
    }]
  },
  {
    "code" : "58",
    "display" : "Reforço Zero",
    "definition" : "R0"
  },
  {
    "code" : "59",
    "display" : "Profilaxia/Tratamento com 1 frasco-ampola/ampola",
    "definition" : "P/T1"
  },
  {
    "code" : "60",
    "display" : "Profilaxia/Tratamento com 2 frascos-ampolas/ampolas",
    "definition" : "P/T2"
  },
  {
    "code" : "61",
    "display" : "Profilaxia/Tratamento com 3 frascos-ampolas/ampolas",
    "definition" : "P/T3"
  },
  {
    "code" : "62",
    "display" : "Profilaxia/Tratamento com 4 frascos-ampolas/ampolas",
    "definition" : "P/T4"
  },
  {
    "code" : "63",
    "display" : "Profilaxia/Tratamento com 5 frascos-ampolas/ampolas",
    "definition" : "P/T5"
  },
  {
    "code" : "64",
    "display" : "Profilaxia/Tratamento com 6 frascos-ampolas/ampolas",
    "definition" : "P/T6"
  },
  {
    "code" : "65",
    "display" : "Profilaxia/Tratamento com 7 frascos-ampolas/ampolas",
    "definition" : "P/T7"
  },
  {
    "code" : "66",
    "display" : "Profilaxia/Tratamento com 8 frascos-ampolas/ampolas",
    "definition" : "P/T8"
  },
  {
    "code" : "67",
    "display" : "Profilaxia/Tratamento com 9 frascos-ampolas/ampolas",
    "definition" : "P/T9"
  },
  {
    "code" : "68",
    "display" : "Profilaxia/Tratamento com 10 frascos-ampolas/ampolas",
    "definition" : "P/T10"
  },
  {
    "code" : "69",
    "display" : "Profilaxia/Tratamento com 11 frascos-ampolas/ampolas",
    "definition" : "P/T11"
  },
  {
    "code" : "70",
    "display" : "Profilaxia/Tratamento com 12 frascos-ampolas/ampolas",
    "definition" : "P/T12"
  },
  {
    "code" : "71",
    "display" : "Profilaxia/Tratamento com 13 frascos-ampolas/ampolas",
    "definition" : "P/T13"
  },
  {
    "code" : "72",
    "display" : "Profilaxia/Tratamento com 14 frascos-ampolas/ampolas",
    "definition" : "P/T14"
  },
  {
    "code" : "73",
    "display" : "Profilaxia/Tratamento com 15 frascos-ampolas/ampolas",
    "definition" : "P/T15"
  },
  {
    "code" : "74",
    "display" : "Profilaxia/Tratamento com 16 frascos-ampolas/ampolas",
    "definition" : "P/T16"
  },
  {
    "code" : "75",
    "display" : "Profilaxia/Tratamento com 17 frascos-ampolas/ampolas",
    "definition" : "P/T17"
  },
  {
    "code" : "76",
    "display" : "Profilaxia/Tratamento com 18 frascos-ampolas/ampolas",
    "definition" : "P/T18"
  },
  {
    "code" : "77",
    "display" : "Profilaxia/Tratamento com 19 frascos-ampolas/ampolas",
    "definition" : "P/T19"
  },
  {
    "code" : "78",
    "display" : "Profilaxia/Tratamento com 20 frascos-ampolas/ampolas",
    "definition" : "P/T20"
  },
  {
    "code" : "79",
    "display" : "Profilaxia/Tratamento com 21 frascos-ampolas/ampolas",
    "definition" : "P/T21"
  },
  {
    "code" : "80",
    "display" : "Profilaxia/Tratamento com 22 frascos-ampolas/ampolas",
    "definition" : "P/T22"
  },
  {
    "code" : "81",
    "display" : "Profilaxia/Tratamento com 23 frascos-ampolas/ampolas",
    "definition" : "P/T23"
  },
  {
    "code" : "82",
    "display" : "Profilaxia/Tratamento com 24 frascos-ampolas/ampolas",
    "definition" : "P/T24"
  }]
}

```
