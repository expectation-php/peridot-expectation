peridot-expectation
===================

Expectation for [peridot](https://github.com/peridot-php/peridot)

[![Latest Stable Version](https://poser.pugx.org/expectation/peridot-expectation/v/stable.svg)](https://packagist.org/packages/expectation/peridot-expectation) [![Latest Unstable Version](https://poser.pugx.org/expectation/peridot-expectation/v/unstable.svg)](https://packagist.org/packages/expectation/peridot-expectation)
[![Dependency Status](https://www.versioneye.com/user/projects/5456291c22b4fba1150002ae/badge.svg?style=flat)](https://www.versioneye.com/user/projects/5456291c22b4fba1150002ae)

[![Build Status](https://travis-ci.org/expectation-php/peridot-expectation.svg?branch=master)](https://travis-ci.org/expectation-php/peridot-expectation)
[![Scrutinizer Code Quality](https://scrutinizer-ci.com/g/expectation-php/peridot-expectation/badges/quality-score.png?b=master)](https://scrutinizer-ci.com/g/expectation-php/peridot-expectation/?branch=master)
[![Coverage Status](https://coveralls.io/repos/expectation-php/peridot-expectation/badge.png?branch=master)](https://coveralls.io/r/expectation-php/peridot-expectation?branch=master)
[![Stories in Ready](https://badge.waffle.io/expectation-php/peridot-expectation.png?label=ready&title=Ready)](https://waffle.io/expectation-php/peridot-expectation)

Installation
------------------

Installation that uses the composer

Please add the following items to composer.json.  
Then please run the composer install.

```php
{
    "require-dev": {
        "expectation/peridot-expectation": "1.2.0"
    }
}
```

Basic usage
------------------

It can be used by simply append the set to **peridot.php**.

```php
use expectation\peridot\ExpectationPlugin;

return function(EventEmitterInterface $emitter) {
    ExpectationPlugin::create()->registerTo($emitter);
};
```

or

How to configure can be found [here](https://github.com/expectation-php/expectation/wiki/Custom-matchers).


```php
use expectation\peridot\ExpectationPlugin;

return function(EventEmitterInterface $emitter) {
    ExpectationPlugin::createWithConfig('.expect.toml')->registerTo($emitter);
};
```




Examples of spec
------------------

You can easily use in the spec file.

```php
describe('Example', function() {
    describe('#create', function() {
        it('return instance', function() {
            expect(Example::create())->toBeAnInstanceOf('Example')
        });
    });
});
```
