# Resources

#### <a id="alert_resource"></a> Alert ####

**Fields :**

| Name | Type | Description |
|------|------|-------------|
| alertID | [ID](./types.md#id_type) | The ID of the alert. |
| contactID | [ID](./types.md#id_type) | The ID of the contact linked with the alert. |
| instrument | String | The instrument to get an alert from. |
| threshold | Float | The threshold to trigger the alert, on the given instrument. |

**Example :**
```js
alert: {
	alertID: "AC15DB",
	contactID: "TD126S",
	instrument: "EURUSD",
	threshold: 1.4950
}
```

<hr />

#### <a id="contact_resource"></a> Contact ####

**Fields :**

| Name | Type | Description |
|------|------|-------------|
| contactID | [ID](./types.md#id_type) | The ID of the contact. |
| civility | String | The civility of the contact. |
| firstName | String | The first name of the contact. |
| lastName | String | The last name of the contact. |
| email | String | The email of the contact. |
| phone | String | The phone number of the contact. |
| tokensAvailable | Integer | The number of alert still available for the contact. |

**Example :**
```js
contact: {
	contactID: "AC15DB",
	civility: "Mr.",
	firstName: "John",
	lastName: "Doe",
	email: "jd@contact.com",
	phone: "+336789456123",
	tokensAvailable: 5
}
```

<hr />

#### <a id="cross_resource"></a> Cross ####

**Fields :**

| Name | Type | Description |
|------|------|-------------|
| instrument | String | The representation of the currency cross with two currencies with [ISO-4217 Currency Code](http://www.xe.com/iso4217.php) format. |

**Example :**
```js
cross: {
	instrument: "EURUSD",
}
```

<hr />

#### <a id="crossList_resource"></a> CrossList ####

**Fields :**

| Name | Type | Description |
|------|------|-------------|
| crossList | Array of [Cross](./resources.md#cross_resource) | An array containing crosses.  |

**Example :**
```js
crossList: [
	{
		instrument: "EURUSD"
	},
	{
		instrument: "EURGBP"
	},
	{
		instrument: "EURHKD"
	},
	...
]
```

<hr />

#### <a id="rate_resource"></a> Rate ####

**Fields :**

| Name | Type | Description |
|------|------|-------------|
| instrument | String | The representation of the currency cross with two currencies with [ISO-4217 Currency Code](http://www.xe.com/iso4217.php) format. |
| rate | Float | The rate of the instrument for the date of the RateHistory. |
| date | [Datetime](./types.md#datetime_type) | The date of the RateHistory. |

**Example :**
```js
rate: {
	instrument: "EURUSD",
	rate: 1.4581,
	date: "2016-01-10 10:15:32"
}
```

<hr />

#### <a id="rateHistory_resource"></a> RateHistory ####

**Fields :**

| Name | Type | Description |
|------|------|-------------|
| rateHistory | Array of [Rate](./resources.md#rate_resource) | An array containing RateHistory.  |

**Example :**
```js
rateHistory: [
	{
		instrument: "EURUSD",
		rate: 1.4581,
		date: "2016-01-10 00:00:00"
	},
	{
		instrument: "EURUSD",
		rate: 1.0154,
		date: "2016-01-11 00:00:00"
	},
	{
		instrument: "EURUSD",
		rate: 1.2458,
		date: "2016-01-12 00:00:00"
	},
	...
]
```

<hr />