# API v1
Base URI &mdash; `https://api.tripteller.co/1/`<br>
While not required, we always suggest using SSL when accessing our API.

## JSONP
If you are unable to use CORS (esp. with older browsers), we support JSONP.

#### Example request
`GET https://api.tripteller.co/1/drugs?callback=done`

#### Example response
    done({
        "drugs": {
            ...
        }
    });
