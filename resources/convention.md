# Conventions

The FX4BIZ public API conforms to the following general behavior for [RESTful API](http://en.wikipedia.org/wiki/Representational_state_transfer):

* You make [HTTPS](http://en.wikipedia.org/wiki/HTTPS) requests to the API endpoint, indicating the desired resources within the URL itself. (The public server, for the sake of security, only accepts [HTTPS](http://en.wikipedia.org/wiki/HTTPS) requests.)
* The [HTTP method](http://en.wikipedia.org/wiki/Hypertext_Transfer_Protocol#Request_methods) identifies what you are trying to do.  Generally, HTTP `GET` requests are used to retrieve information, while HTTP `POST` requests are used to make changes or submit information.
* If more complicated information needs to be sent, it will be included as [JSON-formatted](http://en.wikipedia.org/wiki/JSON) data within the body of the HTTP POST request.
  * This means that you must set `Content-Type: application/json` in the headers when sending POST requests with a body.
* Upon successful completion, the server returns an [HTTP status code](http://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html) of 200 OK, and a `Content-Type` value of `application/json`.  The body of the response will be a JSON-formatted object containing the information returned by the endpoint.

#### Response body ####

**Standard :**  
For relayability and standardizing the API, all the HTTP responses will contain some fields for validation purposes.

| Name | Type | Description |
|------|------|-------------|
| status | Integer | The HTTP status of the request. |
| date | [Datetime](./types.md#datetime_type) | The date when the response was sent by the server. |
| errorMessage | String | A string describing an error if it occurs, null otherwise. |

FX4BIZ uses conventional HTTP response codes to indicate success or failure of an API request. The body of the response contains more detailed information on the cause of the problem.

In general, the HTTP status code is indicative of where the problem occurred:

* Codes in the 200-299 range indicate success. 
    * Unless otherwise specified, methods are expected to return `200 OK` on success.
* Codes in the 400-499 range indicate that the request was invalid or incorrect somehow (e.g. a required parameter was missing, a trade failed, etc.). For example:
    * `400 Bad Request` occurs if the JSON body is malformed. This includes syntax errors as well as when invalid or mutually-exclusive options are selected.
    * `403  Forbidden` occurs if there is a problem with your authentication on the server.
    * `404 Not Found` occurs if the path specified does not exist, or does not support that method (for example, trying to POST to a URL that only serves GET requests)
* Codes in the 500-599 range indicate that the server experienced a problem. This could be due to a network outage or a bug in the software somewhere. For example:
    * `500 Internal Server Error` occurs when the server does not catch an error. This is always a bug. If you can reproduce the error, file it at [our bug tracker in your FX4Biz platform](https://fx4bizplatform.com/login).
    * `502 Bad Gateway` occurs if FX4Biz-REST could not contact its `FX4Biz` server at all.
    * `504 Gateway Timeout` occurs if the `FX4Biz` server took too long to respond to the FX4Biz-REST server.

```js
{
	status: 200,
	date: "2016-05-31 11:22:06",
	errorMessage: null,
	...
}
```

**Success response :**  
For example, if you request the rate for EURUSD, the response will be :
```js
{
	status: 200,
	date: "2016-05-31 11:22:06",
	errorMessage: null,
	rate: {
		instrument: "EURUSD",
		rate: 1.4581,
		date: "2016-01-10"
	}
}
```

**Failed response :**  
If the request fails, here is an example of the response :
```js
{
	status: 400,
	date: "2016-05-31 11:22:06",
	errorMessage: "BAD REQUEST - The instrument you given is an invalid instrument.",
}
```