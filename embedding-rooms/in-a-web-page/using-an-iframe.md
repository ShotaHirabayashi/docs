---
description: >-
  If you want to embed video rooms in a website using HTML or a framework that
  supports HTML elements like React.js, a great option for doing this is by
  using a simple iframe.
---

# Using an iframe

{% embed url="https://youtu.be/kNhhpA_RXg4" %}

Use the `roomUrl` as the `src` attribute as in the example below.

```html
<iframe
  src="https://subdomain.whereby.com/room?minimal"
  allow="camera; microphone; fullscreen; speaker; display-capture; autoplay"
></iframe>
```

When embedding, you can customize the room by [toggling features and behaviors via URL parameters](../../customizing-rooms/using-url-parameters.md).&#x20;

To learn how to restrict which domains are allowed to embed your rooms, read the [Allowed domains section](../allowed-domains.md).
