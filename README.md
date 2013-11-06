# Silex Service-Provider for the Mailchimp-API


##Installation

Add it using [Composer](http://getcomposer.org/) :

```json
{
    "require": {
        "magdev/mailchimp-silex-provider": "dev-master"
    }
}
```

and until this package is registered at [Packagist](https://packagist.org/) add the repository

```json
{
    "repositories" : [{
            "type" : "vcs",
            "url" : "git@github.com:magdev/mailchimp-silex-provider.git"
        }
    ]
}
```

##Usage

###Registering the provider

```php
use Silex\Application;
use SilexMailchimp\Provider\MailchimpServiceProvider;

$app = new Application();
$app->register(new MailchimpServiceProvider(), array(
    'mailchimp.apikey' => 'Your API-Key',
    'mailchimp.options' => array(),  // An array with options for mailchimp/mailchimp
));
```


##License

This package is released under the MIT license