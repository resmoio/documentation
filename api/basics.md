# Basics

### Creating an API Key

You can create your own API Key and access Resmo via Rest API. Creating an API key is easy to manage from **Settings -> Integration -> Rest API Management tab**.&#x20;

Scopes and expiration details of an API key can be managed on this tab. There is also an enable/disable option available for your API key.

### Authentication

In Resmo API, all requests must be authenticated with a bearer token.

Use the HTTP header Authorization with the value Bearer, where the token is the API key you created in Resmo.

{% hint style="info" %}
The API responds with HTTP status 401 in the following conditions;&#x20;

* If the token is absent or invalid
* If the token expired
* If the token is disabled&#x20;
* If the token scope does not valid for the endpoint.
{% endhint %}



