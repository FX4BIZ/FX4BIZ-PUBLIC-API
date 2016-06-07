# Rate

TBD

#### <a id="get_rate"></a> Get rate ####

```http
Method: GET 
URL: /rate/{instrument}/
```
Retrieves the current rate for the instrument given.

**Mandatory parameters:**

| Field | Type | Description |
|-------|------|-------------|
| instrument | String | The representation of the currency pair to get the rate on. |

**Returns:**

An instance of a [Rate](../resources/resources.md#rate_resource) object.

**Example:**
```js
GET /rate/EURUSD/
```

<hr />