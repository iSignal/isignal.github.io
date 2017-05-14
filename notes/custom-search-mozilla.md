== Installing a custom search engine in firefox ==
*May 13 3017*


You may want to customize the search engines that come with your Firefox browser. One reason to do this is to modify the default search query parameters, another would be to add your own custom search engine for a site that does not provide one already. I use this feature to search google for results from the past year alone by default - I find that, especially for tech queries, 4 year old results are mostly inaccurate.

This process is far easier in [Google Chrome](https://www.google/com/chrome). To do this in Firefox, you need to follow these three steps:
1. Install the OpenSearch XML addon from [Firefox's addon repository](https://addons.mozilla.org/en-US/firefox/addon/add-opensearch-xml/).
1. Save XML of the form below, modified for your use case into a local file on your machine. The particular example below allows Firefox to search Google for only past year queries by default.

    >```<OpenSearchDescription xmlns="http://a9.com/-/spec/opensearch/1.1/" xmlns:moz="http://www.mozilla.org/2006/browser/search/"><ShortName>Google-past-year</ShortName><Description>Search Google for last year only</Description><Url method="get" type="text/html" template="https://www.google.com/search?q={searchTerms}&amp;tbs=qdr:y"/></OpenSearchDescription>```
        This XML follows the [OpenSearch XML spec](https://developer.mozilla.org/en-US/Add-ons/Creating_OpenSearch_plugins_for_Firefox).
1. Browse to Firefox->Preferences->Search, click "Add more search engine..." [as shown here](custom-search-mozilla.png). You can set this to be your default engine if you so prefer.


*Sanketh I*
