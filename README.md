# PhpSpec extension for TeamCity CI, supporting phpspec v5 and php 7.1 & 7.2

Formats PhpSpec output to make TeamCity display spec execution results in real-time.

[![Build Status](https://travis-ci.org/dimitri-koenig/teamcity-phpspec-extension.png)](https://travis-ci.org/dimitri-koenig/teamcity-phpspec-extension)

## Installation

Add the following to your composer.json config:

```
    "require": {
        "pawel-grzona/teamcity-phpspec-extension": "dev-master"
    },
    "repositories": [
        {
            "type": "git",
            "url": "https://github.com/dimitri-koenig/teamcity-phpspec-extension"
        }
    ],
```

## Configuration

In your phpspec.yml:

```yml
extensions:
    PhpSpec\TeamCity\Extension: ~
```

## Usage

```bash
./phpspec run -f teamcity
```

## TeamCity Configuration

* Add a Build Step
* Runner Type: Command line
* Run: Custom Script
* Custom Script: `/path/to/phpspec run -f teamcity`
* phpSpec tests will be included in the overall test count along with phpUnit, etc.

## Requirements

PHP 7.1+
