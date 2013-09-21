**THIS IS NOT READY FOR PRODUCTION USE**

[![Build Status](https://travis-ci.org/VeggieMeat/php-taxcloud.png?branch=master)](https://travis-ci.org/VeggieMeat/php-taxcloud)

At this point, most of the functionality needed to complete an order has been
implemented. A few things are still left, including Tax Exemptions and Return
processing.

A smoketest is provided that connects to the TaxCloud API using credentials
stored in environment variables. It is intended for quick tests to ensure that
the core of the library works, but it is not a thorough test. **DO NOT RUN THE
SMOKETEST WITH CREDENTIALS FOR A LIVE SITE. IT WILL CREATE TRANSACTIONS.**

The smoketest also provides an excellent set of examples on how to use this
library.

A "stable" release will be considered when tests cover 90% or more of code,
though 100% coverage is the target.

About
----------------
PHP library to facilitate the ability of your PHP web application to
communicate with TaxCloud.

Compatibility
----------------
php-taxcloud is tested with PHP 5.3 and later.

Contributions
----------------
If you'd like to help with php-taxcloud, your efforts are appreciated!

However, your code should follow PSR-2 guidelines, and API changes must be
accompanied by tests.

Getting Started
----------------
This library requires that you have API credentials for [TaxCloud](https://taxcloud.net) and USPS.

To obtain TaxCloud API keys, you will need to first sign up for an account
with TaxCloud, [verify your website](https://taxcloud.net/account/websites/), and then obtain your **API ID** and **API KEY**
for your specific website.

To obtain a USPS Web Tools **User ID**, you will need to [fill out the form here](https://secure.shippingapis.com/registration/).
You will receive an email with a Username and Password. All you need is the
Username.

Examples
----------------
The smoketest is a great resource for a working example that goes through the
entire process in a basic and straightforward manner. The unit tests are a much
better resource if you need to see how specific functionality works. The unit
tests use stubs to mock the API, and these stubs can show you what sort of data
to expect.

Testing
----------------
php-taxcloud includes thorough unit tests that do not require a live connection
to the API. If you are contributing to php-taxcloud, please include unit tests
for your contributions.

[Travis-ci](https://travis-ci.org/VeggieMeat/php-taxcloud) runs unit tests for the repository. However, you can run them locally
with [PHPUnit](http://phpunit.de/manual/current/en/index.html).

A smoketest is also included that connects to the API and is intended only for
a very quick check that basic functionality has not been broken. To use the
smoketest, you will need to set the following environment variables:
* TaxCloud_apiLoginID
* TaxCloud_apiKey
* TaxCloud_uspsUserID

**DO NOT RUN THE SMOKETEST WITH CREDENTIALS FOR A LIVE SITE. IT WILL CREATE
TRANSACTIONS**
