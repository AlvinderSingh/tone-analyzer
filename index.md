---

copyright:
  years: 2015, 2017
lastupdated: "2017-09-28"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:tip: .tip}
{:pre: .pre}
{:codeblock: .codeblock}
{:screen: .screen}
{:javascript: .ph data-hd-programlang='javascript'}
{:java: .ph data-hd-programlang='java'}
{:python: .ph data-hd-programlang='python'}
{:swift: .ph data-hd-programlang='swift'}

# About

> **Service update:** *The {{site.data.keyword.toneanalyzershort}} service was updated on September 25 and 28, 2017. For the general purpose endpoint, both the request parameters and the response content changed; in addition, the endpoint no longer returns social tones or the disgust tone, and it now accepts French input. Input and throttling limits changed for both endpoints, as did the interface version. The service also now accepts partially correct input instead of returning an error for the overall request. For more information about these and other changes, see the [Release notes](/docs/services/tone-analyzer/release-notes.html).*

The {{site.data.keyword.toneanalyzerfull}} service uses linguistic analysis to detect emotional and language tones in written text. The service can analyze tone at both the document and sentence levels. You can use the service to understand how your written communications are perceived and then to improve the tone of your communications. Businesses can use the service to learn the tone of their customers' communications and to respond to each customer appropriately, or to understand and improve their customer conversations in general.
{: shortdesc}

You submit JSON, plain text, or HTML input that contains your written content to the service. The service accepts up to 128 KB of text, which is about 1000 sentences. The service returns JSON results that report the tone of your input. You can use these results to improve the perception and effectiveness of your communications, ensuring that your writing conveys the tone and style that you want for your intended audience. The following diagram shows the basic flow of calls to the service.

![Submit content to the Tone Analyzer service and use the results to improve your communications.](images/tone-analyzer.png)

## Tone Analyzer endpoints

The service offers two endpoints:

-   **General purpose endpoint** (`GET` or `POST /v3/tone`)

    Use the {{site.data.keyword.toneanalyzershort}} general purpose endpoint to analyze shorter web data, such as email messages or tweets, or longer documents, such as articles or blog posts. Monitor social media to understand what customers are saying about a brand and to determine whom to target with specific messaging. The endpoint accepts JSON, plain text, or HTML input. For more information about the method and the tones that it returns, see [Using the general purpose endpoint](/docs/services/tone-analyzer/using-tone.html).

    The [general purpose demo ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://tone-analyzer-demo.mybluemix.net/){: new_window} lets you submit content to the service for analysis. The service returns overall and sentence-level analyses of the tone of the content.
-   **Customer engagement endpoint** (`POST /v3/tone_chat`)

    Use the {{site.data.keyword.toneanalyzershort}} customer engagement endpoint to monitor customer service and support conversations. Escalate customer conversations when they turn sour or find opportunities to improve customer service scripts, dialog strategies, and customer journeys. The endpoint accepts JSON input. For more information about the method and the tones that it returns, see [Using the customer engagement endpoint](/docs/services/tone-analyzer/using-tone-chat.html).

    The [customer engagement demo ![External link icon](../../icons/launch-glyph.svg "External link icon")](http://customer-engagement-analytics.mybluemix.net/){: new_window} analyzes conversations between customers and customer service agents. The service measures customer satisfaction and concerns, assesses agent performance, and lets you gauge how the interaction evolves.

For information about the pricing plans available for the service, see the [{{site.data.keyword.toneanalyzershort}} service in the {{site.data.keyword.Bluemix_short}} Catalog ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://console.ng.bluemix.net/catalog/services/tone-analyzer){: new_window}.

## Use cases

Some interesting use cases of the service follow:

-   *Social listening and audience monitoring:* Monitor social media to understand what customers are saying about your brand in real-time. For example, you might determine that your customers in Chicago are sad after the Bulls lost or happy during the Taste of Chicago festival. (General purpose endpoint)
-   *Personalized marketing:* Determine whom to target with personalized messaging and when. For example, a travel company might target happy consumers with "treat yourself" messaging, sad consumers with "escape" messaging, and angry consumers with "relax" messaging. (General purpose endpoint)
-   *Chat bots:* Enable an automated agent to detect customer tones and craft suitable responses. For example, you might respond to sadness with "I'm sorry you are upset about this problem" or to satisfaction with "I'm glad you are satisfied with our service." (Customer engagement endpoint)
-   *Customer engagement monitoring and quality assurance:* Monitor the overall tone of agent and customer communications, detect anomalies, and highlight opportunities to train agents on how to better communicate. (Customer engagement endpoint)

You can also use the {{site.data.keyword.toneanalyzershort}} service with additional {{site.data.keyword.ibmwatson_notm}} services, such as [{{site.data.keyword.conversationfull}}](https://console.bluemix.net/docs/services/conversation/index.html) or [{{site.data.keyword.speechtotextfull}}](https://console.bluemix.net/docs/services/speech-to-text/index.html), to analyze user input. For example, the [Conversation Food Coach ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://food-coach.mybluemix.net/){: new_window} application uses the {{site.data.keyword.conversationshort}} service to coach users to make healthy food choices based on their responses about the food that they eat. For more information, see this [Watson blog post ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://developer.ibm.com/watson/blog/2016/10/17/creating-a-compassionate-conversational-agent-using-watson-tone-analyzer-and-watson-conversation-services/){: new_window}.

> **Note:** The {{site.data.keyword.toneanalyzershort}} service algorithmically calculates the tone of written text. It does not infer the personality characteristics of the author of the text. To obtain a personality portrait, see the [{{site.data.keyword.personalityinsightsfull}} service ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://console.bluemix.net/docs/services/personality-insights/index.html){: new_window}.

## Language support
{: #languages}

The `/v3/tone` method can analyze content in English (`en`) and French (`fr`); the `/v3/tone_chat` method supports only English. Both methods can respond with localized content in a variety of languages. For more information, see [Using the general purpose endpoint](/docs/services/tone-analyzer/using-tone.html) and [Using the customer engagement endpoint](/docs/services/tone-analyzer/using-tone-chat.html).
