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

{% api-method method="get" host="https://rapidapi.com" path="/mvp/domain\_status" %}
{% api-method-summary %}
Domain Status
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

{% api-method method="get" host="" path="/mvp/domain\_status\_supported\_tlds" %}
{% api-method-summary %}
Domain Status - Supported TLDs
{% endapi-method-summary %}

{% api-method-description %}
View the TLDs that we are currently able to check availability for. Returns 3 lists:  
1. we can tell that the domain is available or registered, but NOT its expiration date  
2. we can get the expiration date of the domain, AND its availability  
3. we are aware of this domain, but are not able to check its status
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="site\_id" type="string" required=true %}
Optional. Advanced. When you configure your options \(like the TLDs you support and promote\), you get a site\_id and site\_secret token. Pass these variables here, to see which TLDs your site currently supports and promotes.
{% endapi-method-parameter %}

{% api-method-parameter name="site\_secret" type="string" required=true %}
Optional. Your "site\_id" variable is public. It can be used from your client app, and seen by the public. However, this "site\_secret" variable is private. It is used by you, from the back-end, to configure your account options, including supported TLDs. This endpoint only returns a list of your supported TLDs, but you probably don't want anyone to access your business logic.
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

{% api-method method="get" host="" path="/mvp/domain\_whois" %}
{% api-method-summary %}
WhoIS
{% endapi-method-summary %}

{% api-method-description %}
Similar to /domain\_status, but instead of returning a number, this returns the entire WHOIS record, if available.
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



