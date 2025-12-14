Phone Numbers

Search for available numbers



  



        



        



    



        



        



              



        



  



      



              


Search for available numbers

cURL

Copy

```
`curl --request POST \ --url https://api.vogent.ai/api/phone_numbers/search \ --header 'Authorization: Bearer <token>' \ --header 'Content-Type: application/json' \ --data ' { "prefix": "<string>", "country": "US", "limit": 5 } '`
```

200

400

422

Copy

```
`[ { "number": "<string>" } ]`
```

Phone Numbers

# Search for available numbers

Search for available numbers available to purchase

POST

/

phone_numbers

/

search

Try it

Search for available numbers

cURL

Copy

```
`curl --request POST \ --url https://api.vogent.ai/api/phone_numbers/search \ --header 'Authorization: Bearer <token>' \ --header 'Content-Type: application/json' \ --data ' { "prefix": "<string>", "country": "US", "limit": 5 } '`
```

200

400

422

Copy

```
`[ { "number": "<string>" } ]`
```

#### Authorizations

[​](#authorization-authorization)

Authorization

string

header

required

In the form `Bearer <api_key_here>`. You can find your api key in your dashboard.

#### Body

application/json

[​](#body-prefix)

prefix

string

required

The phone number prefix, without the country code.

[​](#body-country)

country

string

default:US

The 2-letter country code.

[​](#body-limit)

limit

integer

default:5

The maximum number of candidates to return, maximum 10.

#### Response

200

application/json

Successful operation

[​](#response-items-number)

number

string

required

The phone number that's available for purchase

[Create a phone number](/api-reference/create-number)[Purchase available number (deprecated, use /phone_numbers instead)](/api-reference/purchase-available-number)