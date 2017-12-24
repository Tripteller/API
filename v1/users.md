# Users
A user is someone who created an account on Tripteller (or [Tripteller Talk](https://talk.tripteller.co)).

| Request | Description |
| --- | --- |
| [GET /users/:id](#get-usersid) | Return a user by its `id` |

#### Variables
| Name | Type | Description |
| --- | --- | --- |
| `id` | integer | The user's unique numeric ID |
| `name` | string | The user's name |
| `banned` | boolean | Whether or not the user is currently banned |
| `name_verified` | boolean | Whether or not the user is [Verified](https://tripteller.co/verified) |
| `name_changed` | date | When the user last changed their `name` (if never, then equal to `created`) |
| `staff` | boolean | Whether or not the user is part of the staff (developers) |
| `moderator` | boolean | Whether or not the user is a Moderator |
| `iq` | integer | The user's total IQ count |
| `avatar` | string | The URL of the user's avatar, or `null` if not set |
| `bio` | string | The user's bio, or `null` if not set |
| `created` | date | When the user created their account |

## `GET /users/:id`
Return a user by its `id`.

#### Example request
    GET https://api.tripteller.co/1/users/1

#### Example response
    {
        "id": 1,
        "name": "Ryan",
        "banned": false,
        "name_verified": true,
        "name_changed": "2017-10-20T04:04:34+00:00",
        "staff": true,
        "moderator": true,
        "iq": 21620,
        "avatar": "https://api.tripteller.co/media/avatars/eb92e442c4660f0545f2e58d645605f3.jpg",
        "bio": "",
        "created": "2017-11-03T22:09:46+00:00"
    }
