# Domain Name APIs

{% api-method method="get" host="https://rapidapi.com" path="/mvp/domain\_suggestions" %}
{% api-method-summary %}
Domain Suggestions
{% endapi-method-summary %}

{% api-method-description %}
Returns lists of domain suggestions. For example, for user entry \`{str:"goodstuff",tld:"info"}\` you may get suggestions \`{"domains": {"list1":\[\],"list2":\[\]}}\`. Also returns work-in-progress phrases used to come up with domain suggestions.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="site\_id" type="string" required=false %}
Optional. Advanced. Use PUT \`/mvp/site/new\` endpoint to register your site. You will receive a unique site\_id token. You may use that in the future to configure options, such as which TLDs you support or wish to promote. Pass that site\_id here, to use your configured options. 
{% endapi-method-parameter %}

{% api-method-parameter name="str" type="string" required=true %}
Second-level domain name,  before the ".com". No sub-domains. Maximum 63 characters. Punctuation is allowed, but will be ignored. Spaces are encouraged! If your visitor types spaces, please keep them, to help us distinguish different words.
{% endapi-method-parameter %}

{% api-method-parameter name="tld" type="string" %}
Top-level domain name. Ex: "com" in "google.com". All TLD extensions are allowed. If we don't have it in our database, the TLD will still be used in suggestions, unless you have set up your own supported TLDs. Default value is "com". 
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

{% api-method method="get" host="https://rapidapi.com" path="/mvp/domain\_suggestions" %}
{% api-method-summary %}
Domain Availability
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter required=true name="str" %}

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

