---
description: >-
  We've compiled some of the most common questions and tips we receive about
  Whereby Embedded.
---

# FAQ & Troubleshooting

You can check for service outages and issues on our status page:

{% embed url="https://wherebystatus.com" %}

{% hint style="danger" %}
We're currently aware of an issue with users running Avast antivirus. The "Avast Web Shield" feature conflicts with sites using port 443 and can cause video feeds to appear as black frames in Whereby. We're working with Avast on a way for them to account for this in their platform, however to resolve Whereby related issues you'll need to disable that feature. [Avast Support Article](https://support.avast.com/en-us/article/antivirus-shield-settings/)
{% endhint %}

### Tips & Tricks

<details>

<summary>Firewall Settings</summary>

To use Whereby behind a firewall, a network administrator will need to adjust the settings. Port 443 will need to be open to all TCP and UDP traffic.\
\
Some enterprise firewalls require more in depth technical information for proper allowance, please contact your Customer Success Manager or embedded@whereby.com

</details>

<details>

<summary>Testing Whereby Embedded</summary>

We always recommend testing Whereby Embedded in an incognito/private browser if possible. If you are logged into your Whereby account, the admin permissions can override some of the features set via parameter or dashboard.

</details>

<details>

<summary>Connections in UAE, China, and Russia</summary>

We're aware of restrictions that have been put in place for peer to peer applications like Whereby. In these areas we've had reports from users that they have spotty access to Whereby, or that the service doesn't work for them at all.&#x20;

Unfortunately, because these are government-level restrictions that have been put in place on the internet, there isn't anything we can do to address issues like this at this time.&#x20;

</details>

### Common Questions

<details>

<summary>Can I customize the page users see when they leave a room?</summary>

Yes! When using our [Embed Element](../embedding-rooms/in-a-web-page/using-the-whereby-embed-element.md) or [Embed SDK](../whereby-embedded-sdk-beta.md#browser-sdk), you'll have access to "leave" browser event. You can then action on that event to redirect your users to another page of your choosing.

</details>

<details>

<summary>URL parameters aren't working as expected</summary>

1. The most common error we see relating to [URL parameters](../customizing-rooms/#using-url-parameters) is incorrectly using "?" twice in the meeting room URL. Combining parameters can be achieved by using the ampersand symbol (&) for example:\
   `?minimal`**`&`**`screenshare=off`.
2. If the person using/testing the room is also logged into their Embedded account, it will override any parameters added to the room URL. Try accessing the room via a private or incognito window to verify your links are working as expected.

</details>

<details>

<summary>Can I create longstanding meetings?</summary>

Yes! You can create meetings with [endDates](../creating-and-deleting-rooms/) far in the future (_eg. A month or multiple months_). Please keep in mind that if you are providing any of your users with [hostUrls](../user-roles-and-privileges.md#hosts), you won't be able to revoke host access from those users.

</details>

<details>

<summary>My hosts/viewers don't have the correct meeting privileges</summary>

1. Host or Viewer privileges will only be available while the room is active and until 1 hour after the meeting's `endDate`
2. Check your [hostRoomUrl](../user-roles-and-privileges.md) or viewerUrl to make sure you've properly separated the `roomkey` and other parameters with "&"

</details>

<details>

<summary>How do I enable integrations in my meetings?</summary>

Integrations are disabled for Whereby Embedded by default while using the [`?minimal`](../customizing-rooms/using-url-parameters.md#minimal) parameter. We set this by default because [Content Security Policy](https://en.wikipedia.org/wiki/Content\_Security\_Policy) restrictions can sometimes cause integrations to fail in unexpected ways. Currently only our YouTube and Miro integrations will work in an embedded setting.

If you would like to test an integration in your embedded meeting, you can do so by adding the `?roomIntegrations=on` parameter.

Please note, we offer limited support for integrations in an embedded meeting, even when enabled. It's highly recommended that you test before using it in a production context.

</details>

<details>

<summary>CORS Policy Error in the browser console</summary>

In some cases you may experience an error in your browsers developer console that looks something like this:

<mark style="color:red;">`Access to fetch at "https://api.whereby.dev/v1/meetings' from origin S° nas WithOutLoginMult:1 been blocked by CORS policy...`</mark>

You need to access the Whereby API from a server environment or computer. You aren't allowed access to the API via the browser console because it would expose your secret API key.

</details>
