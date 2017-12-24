# Classes
A class is a category of [Drugs](/Tripteller/API/blob/master/v1/drugs.md), such as Psychedelics or Opioids.

| Request | Description |
| --- | --- |
| [GET /classes](#get-classes) | Return all classes on Tripteller |
| [GET /classes/:id](#get-classesid) | Return a class by its `id` |

#### Variables
| Name | Type | Description |
| --- | --- | --- |
| id | string | A URL-safe, case-insensitive version of the name |
| name | string | The full name of the class |
| description | string | A Markdown-formatted description for the class |

## `GET /classes`
Return all classes on Tripteller.

#### Example request
    GET https://api.tripteller.co/1/classes

#### Example response
    [
        {
            "id": "depressant",
            "name": "Depressant",
            "description": ""
        },
        ...
    ]

## `GET /classes/:id`
Return a class by its `id`.

#### Example request
    GET https://api.tripteller.co/1/classes/psychedelic

#### Example response
    {
        "id": "psychedelic"
        "name": "Psychedelic"
        "description": ""
    }
