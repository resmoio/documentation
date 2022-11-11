# Basics

### Creating an API Key

You can create your own API Key and access Resmo via Rest API. Creating an API key is an easy step that you can manage from **Settings -> Integration -> Rest API Management tab**.&#x20;

You can manage scopes and expiration details of an API key on this tab. You will also have to enable disable option for your API key.

### Authentication

In Resmo API, all requests must be authenticated with a bearer token.

Use the HTTP header Authorization with the value Bearer, where the token is the API key that you created in Resmo.

{% hint style="info" %}
The API responds with HTTP status 401 in the following conditions;&#x20;

* If the token is absent or invalid
* If the token expired
* If the token is disabled&#x20;
* If the token scope does not valid for the endpoint.
{% endhint %}



