# Account APIs

{% api-method method="put" host="" path="/mvp/account" %}
{% api-method-summary %}
Create a new account
{% endapi-method-summary %}

{% api-method-description %}

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

{% api-method method="post" host="" path="/mvp/account/options" %}
{% api-method-summary %}
Options
{% endapi-method-summary %}

{% api-method-description %}
NOTE: To edit which TLDs you support, including which TLDs you'd like to promote, please refer to the /account/tlds API docs, below.
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

{% api-method method="post" host="" path="/mvp/account/tlds" %}
{% api-method-summary %}
TLDs
{% endapi-method-summary %}

{% api-method-description %}

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



{% api-method method="get" host="" path="/mvp/account/my\_tlds" %}
{% api-method-summary %}
My TLDs
{% endapi-method-summary %}

{% api-method-description %}
See what TLDs you currently have configured, with their preference score. See the \`/account/tlds\` endpoint for more information.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="site\_id" type="string" required=true %}
Advanced. When you created your account, you received a site\_id and site\_secret tokens. Pass these variables here.
{% endapi-method-parameter %}

{% api-method-parameter name="site\_secret" type="string" required=true %}
Your "site\_id" variable is public. It can be used from your client app, and seen by the public. However, this "site\_secret" variable is private. It is used by you, from the back-end, to configure your account options, including supported TLDs. This endpoint only returns a list of your supported TLDs, but you probably don't want anyone to access your business logic.
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Returns an array of TLDs, without the leading dot.
{% endapi-method-response-example-description %}

```
{ data: ["com", "co.uk", "企业"], ... }
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



