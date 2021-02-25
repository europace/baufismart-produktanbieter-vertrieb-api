# Produktanbieter-Vertriebs-Angaben an Vorgängen aktualisieren

Mit dieser API können ausgewählte Produktanbieter im Produktanbieter-Vertrieb spezifische Angaben an Vorgängen auf der
Europace-Plattform aktualisieren.

![Bankeigenvertrieb](https://img.shields.io/badge/-Bankeigenvertrieb-lightblue)
![Baufinanzierung](https://img.shields.io/badge/-Baufinanzierung-lightblue)

[![Authentication](https://img.shields.io/badge/Auth-OAuth2-green)](https://docs.api.europace.de/baufinanzierung/authentifizierung/)
[![GitHub release](https://img.shields.io/github/v/release/europace/baufismart-produktanbieter-vertrieb-api)](https://github.com/europace/baufismart-produktanbieter-vertrieb-api/releases)

[![Pattern](https://img.shields.io/badge/Pattern-Tolerant%20Reader-yellowgreen)](https://martinfowler.com/bliki/TolerantReader.html)

## Dokumentation

[![YAML](https://img.shields.io/badge/OAS-YAML-lightgrey)](https://github.com/europace/baufismart-produktanbieter-vertrieb-api/blob/main/produktanbieter-vertrieb-openapi.yaml)
[![JSON](https://img.shields.io/badge/OAS-JSON-lightgrey)](https://github.com/europace/baufismart-produktanbieter-vertrieb-api/blob/main/produktanbieter-vertrieb-openapi.json)

Feedback und Fragen zum Modell sind
als [GitHub Issue](https://github.com/europace/baufismart-produktanbieter-vertrieb-api/issues/new) willkommen.

## Schnellstart

Damit du unsere APIs und deinen Anwendungsfall schnellstmöglich testen kannst, haben wir
eine [Postman-Collection](https://docs.api.europace.de/baufinanzierung/schnellstart/) für dich zusammengestellt. Diese erlaubt es
dir, Probeaufrufe (Calls) der APIs vorzunehmen. Du kannst dich damit auch an der API authentifizieren.

### Authentifizierung

Bitte
benutze [![Authentication](https://img.shields.io/badge/Auth-OAuth2-green)](https://docs.api.europace.de/baufinanzierung/authentifizierung/)
, um Zugang zur API bekommen. Um die API verwenden zu können, benötigt der OAuth2-Client folgende Scopes:

| Scope                                  | API-Usecase                                                      |
| -------------------------------------- | ---------------------------------------------------------------- |
| `baufinanzierung:vorgang:schreiben`    | Baufinanzierungsvorgänge anlegen                                 |
| `baufinanzierung:echtgeschaeft`        | Vorgänge in Produktion ändern, ansonsten nur Testmodus möglich   |

## Beispiel

Setzen der OLB Bonitätsklasse 6 und Konditionsabschlag für Neukunden:

```json
{
  "scoring": {
    "olb": {
      "bonitaetsklasse": "KLASSE_6"
    }
  },
  "kondition": {
    "olb": {
      "abschlaege": [
        "NEUKUNDE"
      ]
    }
  }
}
```

## Kontakt

Kontakt für Support: [devsupport@europace2.de](mailto:devsupport@europace2.de)

## Nutzungsbedingungen

Die APIs werden unter folgenden [Nutzungsbedingungen](https://docs.api.europace.de/nutzungsbedingungen/) zur Verfügung gestellt.
