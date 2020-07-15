---
description: hostname = ?
---

# Domain Name

{% api-method method="get" host="https://{hostname}" path="/mvp/domain\_suggestions" %}
{% api-method-summary %}
Domain Suggestions
{% endapi-method-summary %}

{% api-method-description %}
Returns lists of domain suggestions. For input \`{str:"hello",tld:"com"}\` you may get suggestions \`{"original phrase":\["hello.fyi","hello.info"\], "word hacks":\["wassupo.com","shalomio.com"\], "": \["aloha.com","shalom.com","hi.co","howdy.io"\]}\`.
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

{% api-method method="get" host="https://{hostname}" path="/mvp/domain\_status" %}
{% api-method-summary %}
Domain Status
{% endapi-method-summary %}

{% api-method-description %}
Returns a dictionary of key/value pairs. 
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter required=true name="str" %}
Domain name to get availability for
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

{% api-method method="get" host="https://{hostname}" path="/mvp/domain\_status\_supported\_tlds" %}
{% api-method-summary %}
Domain Status - Supported TLDs
{% endapi-method-summary %}

{% api-method-description %}
View the TLDs that we are currently able to check availability for. Returns 3 lists:  
1. we can tell that the domain is available or registered, but NOT its expiration date  
2. we can get the expiration date of the domain, AND its availability  
3. we are aware of this domain, but are not able to check its status  
  
Click response below, to see output format:
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{ 
    data: {
        "availability_only": 
                ["ru", "nl", "企业"], 
        
        "availability_and_expiration": 
                ["com", "co.uk", "org",
        
        "nothing": 
                ["中文网", "za.com", "scot"]
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="https://{hostname}" path="/mvp/domain\_whois" %}
{% api-method-summary %}
WhoIS
{% endapi-method-summary %}

{% api-method-description %}
Similar to /domain\_status, but instead of returning a number, this returns the entire WHOIS record, if available.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="str" type="string" required=true %}

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

{% api-method method="get" host="" path="/mvp/domain\_whois\_supported\_tlds" %}
{% api-method-summary %}
WhoIS - Supported TLDs
{% endapi-method-summary %}

{% api-method-description %}
No parameters. Just returns a list of TLDs which we are able to get WHOIS records for.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}

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

