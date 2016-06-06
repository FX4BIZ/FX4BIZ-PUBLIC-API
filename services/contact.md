# Contact

TBD

#### <a id="get_contact"></a> Retrieve contact informations ####

```
Method: GET 
URL: /contact/{type}/{informations}/
```
This request retrieves all informations about a contact.
 
**Mandatory parameters:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| type | String | Mandatory | The type of the search, wether `SMS` or `email`. |
| informations | String | Mandatory | Either the phone number for the type SMS, or the email address for the type email. **Note :** You'll have to URL encode the content of this parameter, due to the variety of character it can contains. |

**Returns:**

An instance of a contact object.

**Example:**
```http
GET /contact/SMS/%2B33123456789
```
```js
{
	contactID: "A145SEA",
	type: "SMS",
	informations: "+33123456789"
}
```

<hr />