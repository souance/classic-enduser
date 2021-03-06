Omeka uses Zend Framework's [ContextSwitch](http://framework.zend.com/manual/en/zend.controller.actionhelpers.html#zend.controller.actionhelpers.contextswitch) action helper to return different response formats on request. Omeka comes bundled with several response formats: omeka-xml, omeka-json, dcmes-xml, json, and rss2. See below for more information about these bundled formats.

To access the response formats, simply add `output=format-name` to the URL query string. For example:
` <http://www.example.com/items/show?output=omeka-xml> `

omeka-xml
-----------------------------------------------------------
The *omeka-xml* response format is an XML instance of the official Omeka omeka-xml schema. It is currently available on the following pages:

-   items/browse
-   items/show
-   files/show

omeka-json
-------------------------------------------------------------
The *omeka-json* response format is a [JsonML](http://jsonml.org/) serialization of the omeka-xml response format. It is currently available on the following pages:

-   items/browse
-   items/show
-   files/show

To enable [JSONP](http://en.wikipedia.org/wiki/JSON#JSONP), you may wrap the JSON output with a callback function by adding
`callback=function-name` to the URL query string. For example:
`<http://www.example.com/items/show?output=omeka-json&callback=foo>`

dcmes-xml
-----------------------------------------------------------
The *dcmes-xml* response format is an [RDF/XML](http://www.w3.org/TR/rdf-syntax-grammar/) instance of [simple Dublin Core](http://dublincore.org/documents/dcmes-xml/). This is the most accurate representation of Omeka's *Dublin Core* element set. It is currently available on the following pages:

-   items/browse
-   items/show

json
-------------------------------------------------
The *json* response format is a streamlined JSON output primarily used for [Ajax](http://en.wikipedia.org/wiki/Ajax_(programming)) requests. There is discussion to deprecate this format once the omeka-json format matures. It is currently available on the following pages:

-   items/show

atom
-------------------------------------------------
The *atom* response format is a commonly used Web content syndication format, [Atom](http://tools.ietf.org/html/rfc4287). It is currently available on the following pages:

-   items/browse
-   items/show

rss2
-------------------------------------------------
The *rss2* response format is a commonly used Web content syndication format, [RSS 2.0](http://cyber.law.harvard.edu/rss/rss.html). It is currently available on the following pages:

-   items/browse
