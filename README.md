# FX4BIZ PUBLIC API

TBD

## API Standards

You can find some standards concerning this API [here](./resources/conventions.md).

## Routes

#### Alert

* [POST /alert/ - Add an alert](./resources/alert.md#post_alert)

#### Contact

* [GET /contact/{type}/{informations}/ - Retrieve contact informations](./services/contact.md#get_contact)
* [POST /contact/ - Add a contact](./services/contact.md#post_contact)

#### Cross

* [GET /cross/ - Get available crosses](./services/cross.md#get_cross)

#### History

* [GET /history/{instrument}/ - Get currency cross history](./services/history.md#get_history)

#### History

* [GET /rate/{instrument}/ - Get rate](./services/rate.md#get_rate)

## Object descriptions

* [Alert](./resources/resources.md#alert_resource)
* [Contact](./resources/resources.md#contact_resource)
* [Cross](./resources/resources.md#cross_resource)
* [CrossList](./resources/resources.md#crossList_resource)
* [Rate](./resources/resources.md#rate_resource)
* [RateHistory](./resources/resources.md#rateHistory_resource)

## Custom types

* [ID](./resources/types.md#id_type)
* [Date](./resources/types.md#date_type)
* [Datetime](./resources/types.md#datetime_type)