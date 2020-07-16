---
description: >-
  This feature is coming soon! Set what TLDs you support and promote. Set many
  other options like min/max length of suggestions, toggle word and domain
  hacks, prefer shorter or more relevant names...
---

# POST to your account

{% api-method method="put" host="https://api.nlp.studio" path="/mvp/account" %}
{% api-method-summary %}
Create a new account
{% endapi-method-summary %}

{% api-method-description %}
coming soon! ...
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="" type="string" required=false %}

{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="post" host="https://api.nlp.studio" path="/mvp/account" %}
{% api-method-summary %}
Options
{% endapi-method-summary %}

{% api-method-description %}
coming soon!
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="" type="string" required=false %}

{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="https://api.nlp.studio" path="/mvp/account" %}
{% api-method-summary %}
Account info, options
{% endapi-method-summary %}

{% api-method-description %}
coming soon!
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="site\_id" required=true %}
When you created your account, you received a site\_id and site\_secret tokens. Pass these variables here.
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-query-parameters %}
{% api-method-parameter name="site\_secret" required=true %}
Your "site\_id" variable is public. It can be used from your client app, and seen by the public. However, this "site\_secret" variable is private. It is used by you, from the back-end, to configure your account options, including supported TLDs. This endpoint only returns a list of your supported TLDs, but you probably don't want anyone to access your business logic.
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

Notes

For added security... With this, you can send this API request directly from your visitor's browser \(front-end code\), without having to waste time routing the user request through your own server. Configure your captcha verification to be very easy to pass if you don't want to annoy your user with that puzzple popup. This trick will work just as well with an easy captcha, because all we're trying to verify is that the request is coming from your own website, and not from a copy/pasted API code on some other website or bot. Configure your captcha version and secret key at: nlp.studio/documentation/account.



