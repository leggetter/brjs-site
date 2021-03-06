---
layout: docs
title: Available Services
permalink: /docs/reference/available_services/
notice: none
---

## EventHub

The service is accessed from the [ServiceRegistry](/docs/concepts/service_registry/) using the `require` service syntax and identifier `br.event-hub`.

```js
var htmlService = require( 'service!br.event-hub' );
```

For full API information see the [EventHub API Docs](http://apidocs.bladerunnerjs.org/latest/js/EventHub.html).

For more information see the [EventHub docs](/docs/concepts/event_hub/).

<a name="HtmlResourceService"></a>
## HtmlResourceService

The HtmlResourceService performs an asynchronous HTTP request and retrieves the HTML bundle file from the app-server.

When HTML is requested from the service, a DOM element is returned.  It is important that you do not make direct changes to the returned DOM element.

Rather, make a copy of it, and make any necessary alterations to the copy. Changes to the original will interfere with other code that requests the same DOM element.

The HTML service translates any embedded internationalisation tokens.

The service is accessed from the [ServiceRegistry](/docs/concepts/service_registry/) using the `require` service syntax and the identifier `br.html-service`.

```js
var htmlService = require( 'service!br.html-service' );
```

For more information see the [HtmlResourceService API Docs](http://apidocs.bladerunnerjs.org/latest/js/HtmlResourceService.html).

## XMLResourceService

Similar to the HtmlResourceService the he XmlResourceService performs an asynchronous HTTP request, and retrieves the XML bundle file from the app-server.

It parses the XML and makes the resulting XML document objects available on request. If you are using JSON based configuration you will not need to use this service.

The service is accessed from the [ServiceRegistry](/docs/concepts/service_registry/) using the `require` service syntax and identifier `br.xml-service`.

```js
var xmlService = require( 'service!br.xml-service' );
```

For more information see the [XmlResourceService API Docs](http://apidocs.bladerunnerjs.org/latest/js/XmlResourceService.html).

## AppMetaService

Provides access to application meta information like the unique version number of the app which is generated by BRJS. In a production environment this will be a timestamp from when the deployed artifact was generated. In development it will be the string *"dev"*.

The service is accessed from the [ServiceRegistry](/docs/concepts/service_registry/) using the `require` service syntax and identifier `br.app-meta-service`.

```js
var appMetaService = require( 'service!br.app-meta-service' );
```

For more information see the [AppMetaService API Docs](http://apidocs.bladerunnerjs.org/latest/js/AppMetaService.html).

## LocaleService

Allows you to retrieve and set the locale being used.

The service is accessed from the [ServiceRegistry](/docs/concepts/service_registry/) using the `require` service syntax and identifier `br.locale-service`.

```js
var localeService = require( 'service!br.locale-service' );
```

For more information see the [AppMetaService API Docs](http://apidocs.bladerunnerjs.org/latest/js/LocaleService.html).
