# Classes
| Request | Description |
| --- | --- |
| [GET /classes](#get-classes) | Return all classes on Tripteller |
| [GET /classes/:id](#get-classesid) | Return a class by its `id` |

## `GET /classes`
Return all classes on Tripteller

#### Example request
    GET https://api.tripteller.co/1/classes

#### Example response
    {
        "classes": [
            {
                "id": "depressant",
                "name": "Depressant",
                "description": null
            },
            ...
        ]
    }

## `GET /classes/:id`
Return a class by its `id`

#### Example request
    GET https://api.tripteller.co/1/classes/psychedelic

#### Example response
    {
        "id": "psychedelic"
        "name": "Psychedelic"
        "description": null
    }
