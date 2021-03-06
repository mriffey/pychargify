Chargify API wrapper for Python
===============================

__Please Note: This library is no longer maintained__

pychargify
----------

This is a Python wrapper for the [Chargify](http://chargify.com) API. It allows you to interface
with the Chargify API using a simple object orientated syntax.

Add customer example

    chargify = Chargify('YOUR-API-KEY', 'YOUR-SUB-DOMAIN')
    
    customer = chargify.Customer()
    customer.first_name = 'John'
    customer.last_name = 'Doe'
    customer.email = 'john@doe.com'
    customer.save()

Create a subscription example:

    customer = chargify.Customer('customer_attributes')
    customer.first_name = 'Paul'
    customer.last_name = 'Trippett'
    customer.email = 'paul@getyouridx.com'
    
    creditcard = chargify.CreditCard('credit_card_attributes')
    creditcard.full_number = 1
    creditcard.expiration_month = 10
    creditcard.expiration_year = 2020

    subscription = chargify.Subscription()
    subscription.product_handle = 'fhaar-mini'
    subscription.customer = customer
    subscription.credit_card = creditcard
    
    subscription.save()

See tests.py for more usage examples.


### Installation

Place this library in your project and import the module

    from pychargify.api import *


### Requirements

This library has no special requirements

### Usage

Simply import this library before you use it:

    from pychargify.api import *
    

Now you'll have access to classes the interact with the Chargify API, such as:

`Chargify`  
`ChargifyProduct`  
`ChargifyCustomer`  
`ChargifiySubscription`
`ChargifiyCreditCard`

`Chargify` is a helper class that makes initialization easier of the `ChargifyProduct`, `ChargifyCustomer`,
`ChargifiySubscription` and `ChargifiyCreditCard` classes


### Contributors

* Paul Trippett (pyhub)  - Base Development
* mrtron - Several Updates and bug fixes to pychargify library
