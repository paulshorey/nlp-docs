# Thesaurus APIs

{% api-method method="get" host="https://api.nlp.studio" path="/mvp/synonyms" %}
{% api-method-summary %}
Synonyms
{% endapi-method-summary %}

{% api-method-description %}
**Most English language words and phrases are supported.** Ex: "appendectomy", "water under the bridge", "hard work", "y'all". Even auxiliary words like "a, an, the, their, which, where" are also supported. More common words will have more synonyms.  
  
**Grouped and sorted by all three:**  
1. parts of speech, starting with the most important part of speech  
2. relevance  
3. length + relevance \(choose short words, which are still relevant\)  
  
This includes all content we have about a word. It can be costly for high volume use. To save money and bandwidth, use /synonyms1, or /synonyms2, or /synonyms3 to limit the results to the specific option of "Grouped and sorted by", explained above.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="word" type="string" required=true %}
Or short phrase. Spaces \(ex: holy moly\) and punctuation \(ex: y'all\) are allowed.
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{
	"data": {
		0: "appendectomy",
		1: {
			"nou": [
				"appendicectomy",
				"hysterectomy",
				"laparotomy",
				"appendix",
				"adenoidectomy",
				"craniectomy",
				"hemorrhoidectomy"
			],
			"bef": [
				"laparoscopic"
			],
			"ver": [],
		},
		2: [
			"appendicectomy",
			"hysterectomy",
			"extirpation",
			"laparotomy",
			"ablation",
			"appendix",
			"cholecystectomy",
			"tonsillectomy",
			"excision",
			"adenoidectomy",
			"craniectomy",
			"hemorrhoidectomy",
			"cutting out"
		],
		3: {
			"appendicectomy",
			"hysterectomy",
			"laparotomy",
			"appendix",
			"adenoidectomy",
			"craniectomy",
			"hemorrhoidectomy"
		},
	}
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="" path="" %}
{% api-method-summary %}
Word Info
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

