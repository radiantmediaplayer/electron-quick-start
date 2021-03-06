# electron-quick-start

This Electron application is based on the [Quick Start Guide](https://electronjs.org/docs/tutorial/quick-start) within the Electron documentation and demonstrates how to use [Radiant Media Player](https://www.radiantmediaplayer.com) with DASH and Widevine DRM.

A basic Electron application needs just these files:

- `package.json` - Points to the app's main file and lists its details and dependencies. In this demo app we use a modified version of Electron which includes all required assets to be Widevine DRM ready.
- `main.js` - Starts the app and creates a browser window to render HTML. In this demo app this is where we prepare our app to be Widevine DRM ready. This is the app's **main process**.
- `index.html` - A web page to render. In this demo app this is where we add our player. This is the app's **renderer process**.

## To Use
From your command line:

```bash
# Clone this repository
git clone https://github.com/radiantmediaplayer/electron-quick-start.git
# Go into the repository
cd electron-quick-start
# Install dependencies
npm install
# Important: Configure index.html with your Radiant Media Player license key
# Run the app
npm start
```

## Documentation for using Radiant Media Player with DASH and Widevine DRM in an Electron app

Our set up is based on [castLabs Electron for Content Security](https://github.com/castlabs/electron-releases). 

In `package.json` you can see that devDependencies for electron points to https://github.com/castlabs/electron-releases#v6.0.4-wvvmp. This set up has been tested with version 6.0.4 of castLabs Electron for Content Security and Radiant Media Player version 5.7.10.

In `index.html` we have our Radiant Media Player configured to use DASH with Widevine DRM with a demo stream. Make sure to add your [PLATFORM Edition license key](https://www.radiantmediaplayer.com/pricing.html) before testing.

In `main.js` we have made changes to automatically prepare our application for Widevine DRM support. 

Please review the above changes before moving forward.

## Supported Widevine DRM features

While this demo app just shows the core principle for using Radiant Media Player with DASH and Widevine DRM, the following features are supported:
- Playback of Widevine DRM encrypted content with DASH (or HLS) 
- Support for Widevine Verified Media Path
- Features generally available with Radiant Media Player when using [DASH and Widevine DRM](https://www.radiantmediaplayer.com/docs/latest/dash-drm-documentation.html)

To achieve this the necessary Widevine DRM components will be installed on first app launch and enabled as an option for playback of DRM protected content using common EME APIs.

For more advanced use-cases see [castLabs Electron for Content Security documentation](https://github.com/castlabs/electron-releases).

Currently unsupported and untested feature with Radiant Media Player:
- Protected storage of licenses for offline playback scenarios

## Supported environments
- Windows 7+
- macOS 10.10+
- Linux Ubuntu 12.04+, Fedora 21+ and Debian 8+ (lacking support for persistent licenses due to VMP limitations)

## License for electron-quick-start
[CC0 1.0 (Public Domain)](LICENSE.md)

## License for Radiant Media Player
Radiant Media Player is a commercial HTML5 media player, not covered by the above CC0 1.0 license. 

Radiant Media Player license can be found here: [https://www.radiantmediaplayer.com/terms-of-service.html](https://www.radiantmediaplayer.com/terms-of-service.html). 

You may request a free trial for Radiant Media Player at: [https://www.radiantmediaplayer.com/free-trial.html](https://www.radiantmediaplayer.com/free-trial.html).
