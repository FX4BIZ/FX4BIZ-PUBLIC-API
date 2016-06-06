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
| type | String | The type of alert, wether `SMS` or `email`. |
| informations | String | Either the phone number for the type SMS, or the email address for the type email. |

**Returns:**

An instance of an [Alert](../resources/resources.md#alert_resource) object.

**Example:**
```js
POST /alert/
{
	contactID: "A145SEA",
	type: "SMS",
	informations: "+33123456789"
}
```

<hr />