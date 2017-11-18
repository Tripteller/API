# Drugs
| Request | Description |
| --- | --- |
| [GET /drugs](#get-drugs) | Return all drugs on Tripteller |
| [GET /drugs/:id](#get-drugsid) | Return a drug by its `id` |

## `GET /drugs`
Return all drugs on Tripteller<br>
#### Parameters
| Key | Optional | Description|
| --- | --- | --- |
| `class` | Yes | Only return drugs by this class |

#### Example request
    GET https://api.tripteller.co/1/drugs?class=psychedelic
#### Example response
    {
        "drugs": [
            {
                "id": "1p-lsd",
                "name": "1P-LSD",
                "alt_names": [],
                "class": {
                    "id": "psychedelic",
                    "name": "Psychedelic",
                    "description": null
                },
                "description": null,
                "dose_material": null,
                "doses": {
                    "light": 0,
                    "normal": 0,
                    "strong": 0,
                    "heavy": 0,
                    "lethal": 0
                },
                "dosing_notes": null
            },
            ...
        }
    }
## `GET /drugs/:id`
Return a drug by its `id`

#### Example request
    GET https://api.tripteller.co/1/drugs/1p-lsd
#### Example response
    {
        "id": "1p-lsd",
        "name": "1P-LSD",
        "alt_names": [],
        "class": {
            "id": "psychedelic",
            "name": "Psychedelic",
            "description": null
        },
        "description": null,
        "dose_material": null,
        "doses": {
            "light": 0,
            "normal": 0,
            "strong": 0,
            "heavy": 0,
            "lethal": 0
        },
        "dosing_notes": null
    }
