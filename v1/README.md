# API v1
Base URI &mdash; `https://api.tripteller.co/1/`

- While not required, we always suggest using SSL when accessing our API.
- All dates are in [ISO 8601](https://www.iso.org/iso-8601-date-and-time-format.html) format and in UTC/GMT.

## JSONP
If you are unable to use CORS (esp. with older browsers), we support JSONP.

#### Example request
`GET https://api.tripteller.co/1/drugs?callback=done`

#### Example response
    drugs([
        {
            "id": "lsd"
            ...
        },
        ...
    ]);
