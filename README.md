# Login OAuth2 Auth0 Plugin

The **Login OAuth2 Auth0** Plugin is for [Grav CMS](http://github.com/getgrav/grav). OAuth2 Provider for Auth0

## Installation

Installing the Login OAuth2 Auth0 plugin can be done in one of two ways. The GPM (Grav Package Manager) installation method enables you to quickly and easily install the plugin with a simple terminal command, while the manual method enables you to do so via a zip file.

### GPM Installation (Preferred)

The simplest way to install this plugin is via the [Grav Package Manager (GPM)](http://learn.getgrav.org/advanced/grav-gpm) through your system's terminal (also called the command line).  From the root of your Grav install type:

    bin/gpm install login-oauth2-auth0

This will install the Login OAuth2 Auth0 plugin into your `/user/plugins` directory within Grav. Its files can be found under `/your/site/grav/user/plugins/login-oauth2-auth0`.

Known issue with gpm installation - https://github.com/getgrav/grav/issues/2833

### Manual Installation

To install this plugin, just download the zip version of this repository and unzip it under `/your/site/grav/user/plugins`. Then, rename the folder to `login-oauth2-auth0`. You can find these files on [GitHub](https://github.com/trilbymedia/grav-plugin-login-oauth2-auth0) or via [GetGrav.org](http://getgrav.org/downloads/plugins#extras).

You should now have all the plugin files under

    /your/site/grav/user/plugins/login-oauth2-auth0
	
> NOTE: This plugin is a modular component for Grav which requires [Grav](http://github.com/getgrav/grav) and the [Error](https://github.com/getgrav/grav-plugin-error) and [Problems](https://github.com/getgrav/grav-plugin-problems) to operate.

### Admin Plugin

If you use the admin plugin manager, you can install directly through the admin panel by browsing the `Plugins` tab and clicking on the `Add` button.

## Configuration

If configuring this plugin via the configuration file, be sure to copy the `user/plugins/login-oauth2-auth0/login-oauth2-auth0.yaml` file to `user/config/plugins/login-oauth2-auth0.yaml` and only edit that copy. This prevents accidental exposure of credentials in the plugins directory via backups or git-sync.

Here is the default configuration and an explanation of available options:

```yaml
enabled: true
client_id: ''
client_secret: ''
domain: ''
scope: ['openid','profile','email']
```
The module is disabled by default. Client Id, Client Secret and Domain can be procured from your Auth0 Dashboard. Scope - don't change this unless you know what you are changing.

When creating your application in Auth0, you can find the callback URLs from the settings in the OAuth2 plugin. If you do not add these to your application as directed by Auth0, the Grav site will not be able to authenticate against Auth0.

Note that if you use the admin user interface to update this plugin, a file with your configuration, and named login-oauth2-auth0.yaml will be automatically saved in the `user/config/plugins/` folder once the configuration is saved in the admin.

## Usage

**Enable the plugin and follow on-screen instructions.**

## Credits
This module wasn't written entirely from scratch. This is largely based on https://github.com/trilbymedia/grav-plugin-login-oauth2-slack . All credits to the original authors.

## To Do

- [ ] Nothing yet.

