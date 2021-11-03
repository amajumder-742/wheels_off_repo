
# Twilio Video Quickstart for JavaScript

## Overview

This is how the application looks like after doing some modification and adding some features from the Examples

![App Interface](https://user-images.githubusercontent.com/90363910/140011806-095298c1-d201-4544-8747-7620d93e2493.png)

## Features 

### Audio Controls after joinig the call 

![Two Participant Joining the call](https://user-images.githubusercontent.com/90363910/140011884-cabf6329-c8f4-4dc9-b3be-9c8442708d48.png)


### Video Controls after joining the call 

![Disabling the Video](https://user-images.githubusercontent.com/90363910/140011888-ab4cd328-0298-447a-b152-5aedf973001a.png)

![Enabling the Video](https://user-images.githubusercontent.com/90363910/140011895-2afb1c64-ab53-4eb7-b17a-4bc50a3deebf.png)


### Taking a Screenshot during an ongoing Video Call 

![Taking Screenshot](https://user-images.githubusercontent.com/90363910/140011903-ea834c93-4447-4610-b792-4551384cf6d2.png)

![Deleting the Screenshot](https://user-images.githubusercontent.com/90363910/140011913-aa9b8b93-253f-478b-a46e-1e3728b30d07.png)

## Setup Requirements

Before we begin, we need to collect all the config values we need to run the application:

- Account SID: Your primary Twilio account identifier - find this [in the console here](https://www.twilio.com/console).
- API Key SID: Used to authenticate - [generate one here](https://www.twilio.com/console/runtime/api-keys).
- API Key Secret: Used to authenticate - [just like the above, you'll get one here](https://www.twilio.com/console/runtime/api-keys).

### A Note on API Keys

When you generate an API key pair at the URLs above, your API Key Secret will only
be shown once - make sure to save this in a secure location,
or possibly your `~/.bash_profile`.

## Setting Up The Application

Create a configuration file for your application:

```bash
cp .env.template .env
```

Edit `.env` with the configuration parameters we gathered from above.

Next, we need to install our dependencies from npm:

```bash
npm install
```

## Running The Application

Now we should be all set! Run the application:

```bash
npm start
```

Your application should now be running at [http://localhost:3000](http://localhost:3000). You will
be prompted to test and choose your microphone and camera. On desktop browsers, your choices will
be saved. _On mobile browsers, you will be asked to test and choose your microphone and camera every
time you load the application in order to make sure they are not reserved by another application_.

After choosing your input devices, you will be prompted to enter your Room name and user name, following
which you will join the Room. Now, all you have to do is open another tab and join the same Room in order
to see and hear yourself on both tabs!

[joinroom.js](quickstart/src/joinroom.js) demonstrates how to use the SDK APIs to build a multi-party
video sesssion. You can start building your own application by incorporating this code into your own
application, and build your user interface around it.

## Running On Multiple Devices

You can use [ngrok](https://ngrok.com/) to try your application
on different devices by creating a secure tunnel to your application server:

```bash
ngrok http 3000
```

You will get a URL of the form `https://a1b2c3d4.ngrok.io` which can be loaded on a browser from a device
different than the one where your application server is running.

## Examples

The project contains some use-case examples for the Twilio Video JS SDK. After running the application
by following the instructions above, go to [http://localhost:3000/examples](http://localhost:3000/examples)
to try them out.
