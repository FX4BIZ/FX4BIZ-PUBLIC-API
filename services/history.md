# History

TBD

#### <a id="get_history"></a> Get currency cross history ####

```http
Method: GET 
URL: /RateHistory/{instrument}/
```
Retrieves the currency cross history for a cross given, with one rate per day.

**Mandatory parameters:**

| Field | Type | Description |
|-------|------|-------------|
| instrument | String | The representation of the currency cross to get history on. |

**Optionnal parameters:**

| Field | Type | Description | Default |
|-------|------|-------------|---------|
| from | [Date](../resources/types.md#date_type) | The starting date to get history on. | One month before the current date. |
| to | [Date](../resources/types.md#date_type) | The ending date to get history on. | The current date. |
| dateFormat | String | A date format expression compatible with [this function](http://php.net/manual/fr/function.date.php). <br />**Note :** You'll have to URL encode the content of this parameter, due to the variety of character it can contains. | `U` |

**Returns:**

An instance of a [RateHistory](../resources/resources.md#rateHistory_resource) object.

**Example:**
```js
GET /history/EURUSD/?from=2016-01-01&to=2016-01-10&dateFormat=Y-m-d
```

<hr />