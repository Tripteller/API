# Drugs
A drug is any psychoactive chemical listed on Tripteller.

| Request | Description |
| --- | --- |
| [GET /drugs](#get-drugs) | Return all drugs on Tripteller |

#### Variables
| Name | Type | Description |
| --- | --- | --- |
| `id` | string | A URL-safe, case-insensitive version of the name |
| `name` | string | The full name of the drug |
| `class` | Class | The class the drug is a part of |
| `description.md` | string | A Markdown-formatted description for the drug |
| `info.json` | string | See https://github.com/Tripteller/Drugs |

## `GET /drugs`
Return all drugs on Tripteller.

#### Parameters
| Name | Type | Description |
| --- | --- | --- |
| `name` | Optional | Search for drugs by name |

#### Example request
    GET https://api.tripteller.co/1/drugs?name=lsd

#### Example response
    [
        {
            "id": "lsd",
            "name": "LSD",
            "class": "psychedelic"
            ...
        },
        {
            "id": "1p-lsd",
            "name": "1P-LSD",
            "class": "psychedelic"
            ...
        },
        ...
    ]
