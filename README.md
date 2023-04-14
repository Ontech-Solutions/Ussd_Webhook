# Ussd Webhook Documentation
## A call back url for a Ussd Remote menu for our tenant clients

Welcome to a documentation on how you can implement your callback url that will receive the request body and return the response body of the format below

### POST request headers

```php
"Accept":"application/json",
"Content_Type":"application/json"
```


### Request Object Body (json)
```json
{
  "REQUEST_TYPE":2,
  "SESSION_ID":"xxxxxxxxxxxxxxxx",
  "MESSAGE":"",
  "MSISDN":"26098383482"
}
```

"SESSION_ID" is a unique session id auto generated by Ontech USSD Gateway
"MESSAGE" is a string coming from the user input into your application
"MSISDN" is the user phone number


### Response Object Body (json)

```json
{
  "ussd_response":{
    "USSD_BODY":"Welcome to ussd testing \n\n1. To Register\n2. To Inquire\n3. Go Back",
    "REQUEST_TYPE":"2"
  }
}
```


### Postman Screenshot
![Test your app](postman.jpg "Postman Screenshot")

#### ONTECH SOLUTIONS
#### https://ontech.co.zm
