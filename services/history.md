# History

TBD

#### <a id="get_history"></a> Get currency cross history ####

```http
Method: GET 
URL: /history/{instrument}
```
Retrieves the currency cross history for a cross given.

**Mandatory parameters:**

| Field | Type | Description |
|-------|------|-------------|
| instrument | String | The representation of the currency cross to get history on. |

**Optionnal parameters:**

| Field | Type | Description | Default |
|-------|------|-------------|---------|
| from | Date | The starting date to get history on. | One month before the current date. |
| to | Date | The ending date to get history on. | The current date. |
| dateFormat | String | A date format expression compatible with [this function](http://php.net/manual/fr/function.date.php). <br />**Note :** You'll have to URL encode the content of this parameter, due to the variety of character it can contains. | `U` |

**Returns:**

An instance of a RateHistoryList object.

**Example:**
```js
GET /history/EURUSD?from=2016-01-01&to=2016-01-10&dateFormat=Y-m-d
```

<hr />