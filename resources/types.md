# Types

### <a id="id_type"></a> ID ###

The ID type describe an identifier for a certain object.

| Type | Real type | format | description | example |
|------|-----------|--------|-------------|---------|
| ID | String | `^[A-Za-z0-9]{*}$` | A String representing the ID of an object. This string contains alpha-numeric characters, including the capital ones. | `ND9dUV` |

<hr />

### <a id="date_type"></a> Date ###

The Date type represents a date with its year, month and day.

| Type | Real type | format | description | example |
|------|-----------|--------|-------------|---------|
| Date | String | `^[0-9]{4}\-[0-9]{2}\-[0-9]{2}$` - `YYYY-MM-DD` | A String representing a date by its year, month and day in month. | `2015-07-14` |

<hr />