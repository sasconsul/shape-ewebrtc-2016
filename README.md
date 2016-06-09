# shape-ewebrtc

## How to send/receive calls in your raspberry pi device using AT&T Enhanced WebRTC

One of the features the AT&T API Platform offers is the Enhanced WebRTC API. This API enables you to integrate real-time audio/video calling into your JavaScript app. After you log in with your Account ID or Virtual Number, your app can send and receive calls to and from any US domestic telephone number, AT&T Virtual Number, or another AT&T Account ID. This article describes the prerequisites and steps necessary to make this happen. For more information on the Enhanced WebRTC API, please refer to the AT&T API Platform section of the AT&T Developer portal.

To simplify your development, the following pre-built components are provided. These can be imported into your JavaScript app project.

Phone – Class used to handle media and networking. Functionality includes starting a session, starting a call, accepting a call, and ending a call.
WebRTCListener – Class used to handle WebRTC events, such as an incoming call.
DhsService - Class used to interact with the Developer Hosted Server (DHS).

## Prerequisite Activity
Before you can begin coding Enhanced WebRTC functionality, you must complete the following prerequisites:

AT&T Developer Portal - Obtain App Key and App Secret

Node Server - Configure and start your Node Server


#### AT&T Developer Portal
To obtain an App Key and App Secret, complete the following steps:

* Sign up on https://developer.att.com if you are not a member yet.
* Log in to the Developer Portal.
* Set up your Account ID domain if you have not already done so.
* Create an app in which to use the Enhanced WebRTC API.
* Make a note of the App Key and App Secret that are generated during this process.

#### Node Server
To configure and start a Node Server using the pre-built Server App, complete the following steps on the device that contains your development environment:

* NodeJS is already installed on the provided AT&T Chromium OS raspberry pi SD cards.
* A pre-built Node Server app with AT&T server-side libraries downloaded on the provided AT&T Chromium OS raspberry pi SD cards.
* Log in to your Chromium device.
* Press CTRL + ALT + T to open terminal.
* In the terminal type `shell` to start running commands.
* Change directory to `/home/chronos/user/` by typing `cd /home/chronos/user/`.
* Configure this instance with the App Key and App Secret you obtained from the AT&T Developer Portal in the previous step.
* Configure the host and port. Use a hostname or IP address that is accessible to your iOS test phone.
* Install the Node dependencies.
* Start the Node Server.
* The pre-built Server App exposes an HTTPS endpoint for Access Token generation, and a e911id generation.

__TIP__: By default, this Server App starts at https://127.0.0.1:9001. However, this address is inaccessible to a real device. To test with a real device, select a hostname or IP address that is accessible to your test phone. For more information on configuring and starting the pre-built Server App, please refer to this documentation on GitHub.

#### You can find more information at the resources listed below.
AT&T Developer Platform
Enhanced WebRTC API
IOS Sample
JavaScript SDK
