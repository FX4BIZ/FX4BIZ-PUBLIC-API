# FX4BIZ PUBLIC API

TBD

## API Standards

You can find some standards concerning this API [here](./resources/convention.md).

## Routes

#### Alert

* [POST /alert/ - Add an alert](./services/alert.md#post_alert)

#### Contact

* [GET /Contact/{type}/{informations}/ - Retrieve contact informations](./services/contact.md#get_contact)
* [POST /Contact/ - Add a contact](./services/contact.md#post_contact)

#### Cross

* [GET /Cross/ - Get available crosses](./services/cross.md#get_cross)

#### History

* [GET /RateHistory/{instrument}/ - Get currency cross history](./services/history.md#get_history)

#### Rate

* [GET /Rate/{instrument}/ - Get rate](./services/rate.md#get_rate)

## Resource description

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