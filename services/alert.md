# Alert

TBD

#### <a id="post_alert"></a> Add an alert ####

```
Method: POST 
URL: /alert/
```
Adds an alert for the contact given, with the parameters given.

**Mandatory parameters:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| contactID | ID | Mandatory | The ID of the contact to add the alert. | 
| type | String | Mandatory | The type of alert, wether `SMS` or `email`. |
| informations | String | Mandatory | Either the phone number for the type SMS, or the email address for the type email. |

**Returns:**

An instance of an alert object.

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