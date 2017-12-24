# Drugs
| Request | Description |
| --- | --- |
| [GET /drugs](#get-drugs) | Return all drugs on Tripteller |
| [GET /drugs/:id](#get-drugsid) | Return a drug by its `id` |

## `GET /drugs`
Return all drugs on Tripteller.

#### Parameters
| Name | Type | Description |
| --- | --- | --- |
| `class` | Optional | Only return drugs by this class |

#### Response
| Name | Type | Description |
| --- | --- | --- |
| `id` | string | A URL-safe, case-insensitive version of the name |
| `name` | string | The full name of the drug |
| `alt_names` | array | A list of alternative names for the drug |
| `class` | [Class](/Tripteller/API/blob/master/v1/classes.md) | The class this drug is a part of |
| `description` | string | A Markdown-formatted description for this drug |
| `doses` | object | Doses in micrograms (plus material) for each ROA |
| `dosing_notes` | string | Information on dosing this drug |
| `image` | string | An SVG image of the drug's chemical structure |

#### Example request
    GET https://api.tripteller.co/1/drugs

#### Example response
    [
        {
            "id": "lsd",
            "name": "LSD",
            "alt_names": [
                "Lucy",
                "acid",
                "tabs",
                "stamps"
            ],
            "class": {
                "id": "psychedelic",
                "name": "Psychedelic",
                "description": ""
            },
            "description": "",
            "doses": {
                "oral": {
                    "light": 25,
                    "normal": 75,
                    "strong": 150,
                    "heavy": 400,
                    "lethal": null,
                    "material": null
                },
                "buccal": {
                    "light": 25,
                    "normal": 75,
                    "strong": 150,
                    "heavy": 400,
                    "lethal": null,
                    "material": null
                },
                "rectal": null,
                "snorted": null,
                "inhaled": null,
                "iv": null
            },
            "dosing_notes": "",
            "image": "https://api.tripteller.co/media/structures/lsd.svg"
        },
        ...
    ]
## `GET /drugs/:id`
Return a drug by its `id`.

#### Example request
    GET https://api.tripteller.co/1/drugs/kratom

#### Example response
    {
        "id": "kratom",
        "name": "Kratom",
        "alt_names": [
            "mitragynine",
            "ketum"
        ],
        "class": {
            "id": "opioid",
            "name": "Opioid",
            "description": ""
        },
        "description": "",
        "doses": {
            "oral": {
                "light": 2000000,
                "normal": 3000000,
                "strong": 5000000,
                "heavy": 8000000,
                "lethal": null,
                "material": "dried leaf"
            },
            "buccal": null,
            "rectal": null,
            "snorted": null,
            "inhaled": null,
            "iv": null
        },
        "dosing_notes": "",
        "image": "https://api.tripteller.co/media/structures/kratom.svg"
    }
