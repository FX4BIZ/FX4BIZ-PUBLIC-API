# Alert

TBD

#### <a id="post_alert"></a> Add an alert ####

```http
Method: POST 
URL: /alert/
```
Adds an alert for the contact given, with the parameters given.

**Mandatory parameters:**

| Field | Type | Description |
|-------|------|-------------|
| contactID | [ID](../resources/types.md#id_type) | The ID of the contact to add the alert. | 
| instrument | String | The instrument to get an alert from. |
| threshold | Float | The threshold to trigger the alert, on the given instrument. |

**Returns:**

An instance of an [Alert](../resources/resources.md#alert_resource) object.

**Example:**
```js
POST /alert/
{
	contactID: "A145SEA",
	instrument: "EURUSD",
	threshold: 1.4950
}
```

<hr />