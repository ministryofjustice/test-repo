Test Repo [![Latest Stable Version](https://poser.pugx.org/genesis/behat-fail-aid/v/stable)](https://packagist.org/packages/genesis/behat-fail-aid) [![Total Downloads](https://poser.pugx.org/genesis/behat-fail-aid/downloads)](https://packagist.org/packages/genesis/behat-fail-aid) [![License](https://poser.pugx.org/genesis/behat-fail-aid/license)](https://packagist.org/packages/genesis/behat-fail-aid) [![Monthly Downloads](https://poser.pugx.org/genesis/behat-fail-aid/d/monthly)](https://packagist.org/packages/genesis/behat-fail-aid) [![Quality Gate Status](https://sonarcloud.io/api/project_badges/measure?project=forceedge01_behat-fail-aid&metric=alert_status)](https://sonarcloud.io/dashboard?id=forceedge01_behat-fail-aid) [![Maintainability Rating](https://sonarcloud.io/api/project_badges/measure?project=forceedge01_behat-fail-aid&metric=sqale_rating)](https://sonarcloud.io/dashboard?id=forceedge01_behat-fail-aid) [![Security Rating](https://sonarcloud.io/api/project_badges/measure?project=forceedge01_behat-fail-aid&metric=security_rating)](https://sonarcloud.io/dashboard?id=forceedge01_behat-fail-aid)
=======

Introduction
-------------

Time and time again we've all seen how difficult and stressful it can become to fix behat tests. This package is their to help gather
all possible information around failures and print them as you see a failure taking out the need to do basic investigations with minimal setup.

Usual failure
![Before](https://raw.githubusercontent.com/forceedge01/behat-fail-aid/master/extras/generic-from.png#version=1)

With fail-aid context
![After](https://raw.githubusercontent.com/forceedge01/behat-fail-aid/master/extras/generic-to.png#version=1)

With config options enabled
![More info](https://raw.githubusercontent.com/forceedge01/behat-fail-aid/master/extras/max-details.png#version=1)

The links are ready to be clicked on and opened in the browser. No faff!

You also get the following step definitions for free upon activation:

```gherkin
And I take a screenshot
And I gather facts for the current state
```

These will output relevant information on the screen. (Your formatting must be pretty for this to work --format=pretty).

Whats new:
----------

Major: Refactor, Controlled output, scenario debug cli, clear screenshots cli, host machine screenshot url.

Minor: 
- Resolve environment variables for hostUrl and hostDirectory options.
- Execute screenshot code only if requested in output.
- Override output parameters through individual context file params.
- Override more output parameters.
- Set output.api parameter to true to set all mink related flags/operations to false for quick settings.

Patch: NA.

Installation:
-------------
```shell
composer require genesis/behat-fail-aid --dev
```

Development
-----------

To develop locally, you'll need the following:

- php7.0+
- composer (package manager)

Install project dependencies using composer:

```
composer install
```

Unit tests can be triggered using the following command:

```
./vendor/bin/phpunit -c tests
```

Behaviour tests

```
./vendor/bin/behat -c behat.yml
```

More information on how to run tests can be found in the Makefile or docker-compose file.
