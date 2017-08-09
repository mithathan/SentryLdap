# SentryLdap

SentryLdap is a fork of Cartalyst Sentry library. Added new features like ldap authentication.SentryLdap is a PHP 5.3+ fully-featured authentication & authorization system. It also provides additional features such as user groups and additional security features.

This branch works with Laravel 5.3 !

Sentry is a framework agnostic set of interfaces with default implementations, though you can substitute any implementations you see fit.

### Features

It also provides additional features such as user groups and additional security features:
- Ldap login

Sentry features
- Configurable authentication (can use any type of authentication required, such as username or email)
- Authorization
- Activation of user *(optional)*
- Groups and group permissions
- "Remember me"
- User suspension
- Login throttling *(optional)*
- User banning
- Password resetting
- User data
- Interface driven - switch out your own implementations at will

### Installation

Installation of SentryLdap is very easy. Open your composer.json file and add the following to the require array:

    "mithat/sentry_ldap_for_laravel_5": "2.3.*"

to your composer.json file then follow one of the following guides to get SentryLdap working with your favorite framework.

For more information about Sentry, you must visit the sentry web site:
https://cartalyst.com/manual/sentry/2.1

### Using

This library is still beta for ldap functions. You have to change this lines in your config file.

	'ldap' => array(
		'server'	=> 'ldapserver',
		'port'		=> 'ldapport'
	),

After this settings you have to follow sentry orginal document file. You can use ldap login like this;

    // Set login credentials
    $credentials = array(
        'userid'    => 'demo',
        'password' => 'demo',
    );

    // Try to authenticate the user
    $user = Sentry::authenticateWithLdap($credentials, false);

Also have Sentry::authenticateWithLdapAndRemember($credentials); function.


### Support

We offer support through [our help forums](http://help.cartalyst.com), on [IRC at #cartalyst](http://webchat.freenode.net/?channels=cartalyst) for normal sentry issues, and through GitHub issues (bugs only) for Ldap issues.