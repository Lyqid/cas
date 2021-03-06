---
layout: default
title: CAS - Web Flow Customization
category: Webflow Management
---

{% include variables.html %}

# Webflow Errors Customization

By default CAS is configured to recognize and handle a number of exceptions for web flow during authentication. Each exception has the specific message bundle mapping in `messages.properties` So that a specific message could be presented to end users on the login form. Any un-recognized or un-mapped exceptions results in the `UNKNOWN` mapping with a generic `Invalid credentials.` message.

To map custom exceptions in the webflow, one would need map the exception in CAS settings and then define the relevant error in `messages.properties`:

```properties
authenticationFailure.MyAuthenticationException=Authentication has failed, but it did it my way!
```

{% include casproperties.html properties="cas.authn.errors" %}

