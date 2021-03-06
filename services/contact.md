# Contact

TBD

#### <a id="get_contact"></a> Retrieve contact informations ####

```http
Method: GET 
Path: /Contact/{type}/{informations}/
```
This request retrieves all informations about a contact.
 
**Mandatory parameters:**

| Field | Type | Description |
|-------|------|-------------|
| type | String | The type of the search, wether `SMS` or `email`. |
| informations | String | Either the phone number for the type SMS, or the email address for the type email.<br />**Note :** You'll have to URL encode the content of this parameter, due to the variety of character it can contains. |

**Returns:**

An instance of a [Contact](../resources/resources.md#contact_resource) object.

**Example:**
```js
GET /Contact/SMS/+336123456789
```

<hr />

#### <a id="post_contact"></a> Add a contact ####

```http
Method: POST 
Path: /contact/
```
This request adds a contact.
 
**Mandatory parameters:**

| Field | Type | Description |
|-------|------|-------------|
| civility | String | The civility of the contact, wether `Mr.` or `Mrs.`. |
| firstName | String | The first name of the contact. |
| lastName | String | The last name of the contact. |
| type | String | The type of the contact, wether `SMS` or `email`. |
| informations | String | Either the phone number for the type SMS, or the email address for the type email. |

**Returns:**

An instance of a [Contact](../resources/resources.md#contact_resource) object.

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