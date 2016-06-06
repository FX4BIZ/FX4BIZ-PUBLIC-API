# Contact

TBD

#### <a id="get_contact"></a> Retrieve contact informations ####

```http
Method: GET 
Path: /contact/{type}/{informations}/
```
This request retrieves all informations about a contact.
 
**Mandatory parameters:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| type | String | Mandatory | The type of the search, wether `SMS` or `email`. |
| informations | String | Mandatory | Either the phone number for the type SMS, or the email address for the type email.<br />**Note :** You'll have to URL encode the content of this parameter, due to the variety of character it can contains. |

**Returns:**

An instance of a contact object.

**Example:**
```js
GET /contact/SMS/+336123456789
```

<hr />

#### <a id="post_contact"></a> Add a contact ####

```http
Method: POST 
Path: /contact/
```
This request adds a contact.
 
**Mandatory parameters:**

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| civility | String | Mandatory | The civility of the contact, wether `Mr.` or `Mrs.`. |
| firstName | String | Mandatory | The first name of the contact. |
| lastName | String | Mandatory | The last name of the contact. |
| type | String | Mandatory | The type of the search, wether `SMS` or `email`. |
| informations | String | Mandatory | Either the phone number for the type SMS, or the email address for the type email. |

**Returns:**

An instance of a contact object.

**Example:**
```js
POST /contact/
{
	civility: "Mr.",
	firstName: "John",
	lastName: "Doe",
	type: "email",
	informations: "jd@contact.com"
}
```

<hr />