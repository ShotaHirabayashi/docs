---
description: >-
  With Whereby Embedded you can use URL parameters to customize the meeting
  experience for your users. It’s possible for each participant in a meeting to
  have different parameter combinations.
---

# Using URL parameters

URL parameters are added to the `roomURL` when embedding a room in your web page or app.

Several parameters can be combined by using the ampersand symbol (&). For instance, the following URL parameters would open the room with the screenshare and people buttons hidden:

```
https://subdomain.whereby.com/room?screenshare=off&people=off
```

## URL parameters

| URL Parameter                                                                                                      | Description                                                                                 |
| ------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------- |
| [`?minimal`](using-url-parameters.md#minimal)                                                                      | Applies a minimal UI. Turns off all controls except for cam and mic.                        |
| [`?video=off`](using-url-parameters.md#video-off)                                                                  | Participant joins the room with camera turned off.                                          |
| [`?audio=off`](using-url-parameters.md#audio-off)                                                                  | Participant joins the room with microphone turned off.                                      |
| [`?cameraAccess=<on\|off>`](using-url-parameters.md#cameraaccess-less-than-on-or-off-greater-than)                 | Camera permissions are not requested or used at all. On by default.                         |
| [`?screenshare=<on\|off>`](using-url-parameters.md#screenshare-less-than-on-or-off-greater-than)                   | Show/hide the screenshare[^1] button.                                                       |
| [`?chat=<on\|off>`](using-url-parameters.md#chat-less-than-on-or-off-greater-than)                                 | Show/hide the chat button.                                                                  |
| [`?people=off`](using-url-parameters.md#chat-less-than-on-or-off-greater-than)                                     | Hide the people button.                                                                     |
| [`?leaveButton=<on\|off>`](using-url-parameters.md#leavebutton-off)                                                | Show/hide the leave button.                                                                 |
| [`?displayName=<name>`](using-url-parameters.md#displayname-less-than-name-greater-than)                           | Set display name of participant.                                                            |
| [ `?avatarUrl=<url>`](using-url-parameters.md#avatarurl-less-than-url-greater-than)                                | Set the profile avatar of participant.                                                      |
| [`?background=off`](using-url-parameters.md#background-off)                                                        | Hide the room background.                                                                   |
| [`?logo=off`](using-url-parameters.md#logo-off)                                                                    | Hide the logo in the room header.                                                           |
| [`?locking=off`](using-url-parameters.md#locking-off)                                                              | Hide the room lock button.                                                                  |
| [`?participantCount=off`](using-url-parameters.md#participantcount-off)                                            | Hide the participant counter.                                                               |
| [`?settingsButton=off`](using-url-parameters.md#settingsbutton-off)                                                | Hide the settings button.                                                                   |
| [`?pipButton=off`](using-url-parameters.md#pipbutton-off)                                                          | Hide the Picture in Picture button.                                                         |
| [`?moreButton=off`](using-url-parameters.md#morebutton-off)                                                        | Hide the more button.                                                                       |
| [`?topToolbar=<on\|off>`](using-url-parameters.md#toptoolbar-less-than-on-or-off-greater-than)                     | Show/hide the entire top toolbar.                                                           |
| [`?bottomToolbar=<on\|off>`](using-url-parameters.md#bottomtoolbar-less-than-on-or-off-greater-than)               | Show/hide the entire bottom toolbar.                                                        |
| [`?lang=<code>`](using-url-parameters.md#lang-less-than-code-greater-than)                                         | Set the room UI language.                                                                   |
| [`?floatSelf`](using-url-parameters.md#floatself)                                                                  | Float the self view to the bottom right.                                                    |
| [`?breakout=<on\|off>`](using-url-parameters.md#breakout-less-than-on-or-off-greater-than)                         | Show/hide the breakout room feature for the meeting host.                                   |
| [`?groups=Orange,Banana,Coconut`](using-url-parameters.md#groups-orange-banana-coconut)                            | Predefine up to 20 groups for the breakout groups function.                                 |
| [`?timer=<on\|off>`](using-url-parameters.md#timer-less-than-on-or-off-greater-than)                               | Show/hide the meeting timer.                                                                |
| [`?precallReview=<on\|off>`](using-url-parameters.md#precallreview-less-than-on-or-off-greater-than)               | Determines if users see the pre-call review step.                                           |
| [`?skipMediaPermissionPrompt`](using-url-parameters.md#skipmediapermissionprompt)                                  | Skips the request permissions UI and asks for devices                                       |
| [`?subgridLabels=<on\|off>`](using-url-parameters.md#subgridlabels-less-than-on-or-off-greater-than)               | Enable name labels for participants in the subgrid                                          |
| [`?metadata=<string>`](using-url-parameters.md#metadata-less-than-string-greater-than)                             | Gets passed on to the corresponding webhooks.                                               |
| [`?lowData=<on\|off>`](using-url-parameters.md#lowdata-less-than-on-or-off-greater-than)                           | Use a lower resolution by default                                                           |
| [`?autoSpotlight`](using-url-parameters.md#autospotlight)                                                          | Automatically spotlight the local participant on room join                                  |
| [`?roomIntegrations=on`](using-url-parameters.md#roomintegrations)                                                 | Enables YouTube and Miro integrations in the meeting                                        |
| [`?virtualBackgroundUrl=<url>`](using-url-parameters.md#virtualbackgroundurl-less-than-url-greater-than)           | Specify custom virtual background which should be applied to the local participant          |
| [`?precallPermissionHelpLink=<url>`](using-url-parameters.md#precallpermissionhelplink-less-than-url-greater-than) | Specify custom help link in pre-call review step pointing users to additional support pages |
| [`?precallCeremony=<on\|off>`](using-url-parameters.md#precallceremony-less-than-on-or-off-greater-than)           | Determines if users see the pre-call device and connectivity test.                          |

## Property details

#### `?minimal`

The minimal parameter applies a combination of UI adjustments to simplify the embedded meeting interface.

**Hidden items:** Status bar, chat button, screensharing button, leave button, and Whereby’s branding.

**Shown items:** Video and audio buttons.

For further adjustments, additional parameters can be combined with `?minimal`. For example\
`?minimal&chat=on` will show the chat button.

#### `?video=off`

Participants join the meeting with their camera off, they can turn it on whenever they want.

**Use case:** A sales representative showcasing a product to a customer relaxing at home.

#### `?audio=off`

Participants join the meeting with their microphone off, they can turn it on whenever they want.

**Use case:** A presentation is being given in a big meeting where attendees are not expected to participate verbally.

#### `?cameraAccess=<on|off>`

Whereby will not request access to participants' cameras when this is set to off, and there are no video controls.

**Use case:** A voice-only meeting where attendees are not expected to show themselves on camera.

#### `?screenshare=<on|off>`

Show/hide the screensharing button for the meeting participant.

Screensharing is available on all browsers that support this natively. Currently no mobile browsers support screensharing.

#### `?chat=<on|off>`

Show/hide the chat button. Messages are not stored after the meeting has ended.

#### `?people=off`

Hide the people button.

**Use case:** The people button shows the participant list, which can be useful for bulk management of participants in bigger meetings.

#### `?leaveButton=off`

Hide the leave button.

**Use case:** Can be used if you want to control the leave flow in other ways, like adding a custom link or button outside the embedded room to control what happens when users leave the call.

#### `?displayName=<name>`

Set the display name for a participant instead of prompting the user for this information.

**Use case:** A participant’s name may be known before they join the meeting. Including this information as a parameter will save the user from entering their name again.

#### **`?avatarUrl=<url>`**

Set the avatar / profile picture of the participant instead of the automatically assigned name initials. The image can be a .png or .jpeg, and must be a square maximum of 64x64.

**Note:** You must make sure to list the origin of the image URL in the [allowed domains](../embedding-rooms/allowed-domains.md) section of the dashboard. The image URL must be https and cannot contain query params.

#### `?background=off`

Hide the default meeting background.

**Use case:** Hiding the meeting background allows the meeting to appear more integrated by allowing the app or service’s branding shine through as the new background.

#### `?logo=off`

Hide the logo in the room header.

**Use case:** Control whether or not your company logo is displayed in the room header.

#### `?locking=off`

Hide the room lock button.

**Use case:** When set to off the lock button won’t be displayed in the room header. Also, hosts won’t be able to lock/unlock the room through the settings menu or the keyboard shortcut.

#### `?participantCount=off`

Hide the participant counter.

**Use case:** Will display the current and maximum number of participants in the room, e.g. “2/4” or “13/200”.

#### `?settingsButton=off`

Hide the settings button.

**Use case:** Control whether or not the settings button is displayed in the room header.

#### `?pipButton=off`

Hide the Picture in Picture button.

**Use case:** Control whether or not the Picture in Picture button is displayed in the room header. Picture in Picture lets you pop out your meeting guests’ faces while browsing other tabs or applications.

#### `?moreButton=off`

Hide the “…” button.

**Use case:** Control whether or not the “…” button is displayed in the room header.

#### `?topToolbar=<on|off>`

Used to toggle the entire top toolbar on/off.

**Use case:** When using the [`minimal`](using-url-parameters.md#minimal) parameter, the top toolbar is hidden along with many other UI elements. Using `topToolbar=on` will cause the top toolbar to display, which is required if you want to enable breakout groups using [`breakout=on`](using-url-parameters.md#breakout-less-than-on-or-off-greater-than).

#### `?bottomToolbar=<on|off>`

Show/hide the entire bottom tool bar.

**User case:** Hiding the bottom toolbar entirely can be useful in cases where you are hoping to control in room items like camera or microphone via your own websites UI. This can be achieved when embedding Whereby with the [Whereby Embed Element](../embedding-rooms/in-a-web-page/using-the-whereby-embed-element.md).

#### `?lang=<code>`

Set the meeting UI language to match your product or service. Select from either English `en`, French `fr`, Italian `it`, German `de`, Norwegian `nb`, Dutch `nl`, Portuguese `pt`, Polish `pl`, Spanish `es`, Hindi `hi`, Czech `cs`, or Japanese `jp`.

#### `?floatSelf`

Float the self view to the bottom right.

**Use case:** Floating the self view to the bottom right maximizes the space for other meeting participants.

#### `?breakout=<on|off>`

Show/hide the [Breakout Groups feature](breakout-groups-with-embedded.md) for the meeting host.

**Use case:** Combine bigger meetings with smaller, collaborative sessions. Your hosts can start breakout sessions where participants are split into smaller groups.

#### `?groups=Orange,Banana,Coconut`

Predefine up to 20 groups for the breakout groups function.

**Use case:** Setting up groups ahead of time can save the host time during the meeting. Hosts will still be able to modify the group setup during the session using the in-room controls if needed.

#### `?timer=<on|off>`

Show/hide the meeting timer within the room.

**Use case:** Set this to “on” to have the meeting timer be displayed in the room. When set to “off”, room hosts can still activate the meeting timer from the “…” button, unless this button has been hidden via the `?minimal` or `?moreButton=off` parameters.

#### `?precallReview=<on|off>`

Determines if users see the pre-call review step.

**Use case:** The pre-call review step will allow users to check their video/audio settings before joining the room, but this can be skipped by setting this parameter to “off”.

#### `?precallCeremony=<on|off>`

Determines if users see the pre-call device and connectivity test.

**Use case:** The pre-call test will provide users a test of each device; camera, microphone, and speakers, before joining the room. It will also run a connectivity test to assess the reliability of the participants network. This can be skipped by setting this parameter to “off”.

#### **`?skipMediaPermissionPrompt`**

Skips the request permissions UI and asks for devices

**Use case:** This parameter will prevent the "Request Permissions" step during the pre-call phase and cause the browser to automatically request device permissions (if requested in the iFrame). This flag is required for [Android app](../embedding-rooms/in-a-mobile-app/in-android-apps.md) integration.

#### `?subgridLabels=<on|off>`

Used to toggle name labels for the participants in the subgrid.

**Use case:** Set this to “on” to show name labels for the participants that are rendered as small tiles in the subgrid. Makes it easier to distinguish participants with their camera off.

#### `?metadata=<string>`

Can be used to pass any URL-encoded string so that it is included in the corresponding webhooks. The decoded string has a **limit of 512 characters**.

**Use case:** Set it to the user’s ID so that you can easily track through [webhooks](../monitoring-usage/webhooks.md) when a particular user joins or leaves a room.

#### `?lowData=<on|off>`

Use a lower resolution by default

**Use case:** In some situations for users with poor network connections or devices with CPU constraints, it can be helpful to have lower resolution video feeds loading on the call. This can alleviate problems for users reporting issues with choppy video/audio or connecting to rooms.

#### **`?autoSpotlight`**

Automatically spotlight the local participant on room join.&#x20;

**Note:** Only works when the participant joining has host privileges.\
\
**Use case:** Apply this parameter to ensure focus is directed at the local participant by spotlighting them. The spotlight ensures everyone else in the meeting has a bigger view of this participant.

#### `?roomIntegrations`

Integrations are disabled for Whereby Embedded by default while using the [`?minimal`](using-url-parameters.md#minimal) parameter. We set this by default because [Content Security Policy](https://en.wikipedia.org/wiki/Content\_Security\_Policy) restrictions can sometimes cause integrations to fail in unexpected ways. Currently **only our YouTube and Miro** integrations will work in an embedded setting.

It is recommended you do testing to verify these integrations behave as expected before releasing to your users.

#### **`?virtualBackgroundUrl=<url>`**

Specify a image url to use as the virtual background for the participant. The image must be provided in **1280x720** resolution in either `image/jpeg` or `image/png` format. In addition, the image should be retrievable using CORS.

#### `?precallPermissionHelpLink=<url>`

Specify custom help link on the pre-call review step pointing users to additional support pages. This parameter should only be applied when pre-call review is enabled. This preference can also be set globally via the [Dashboard](dashboard-preferences.md#help-me-fix-this).

**Use case:** Apply this parameter to point users with camera or mic permission problems to bespoke [help pages](../faq-and-troubleshooting/end-user-documentation.md) published on your own domain and brand, rather than to Whereby's help docs.&#x20;

[^1]: 
