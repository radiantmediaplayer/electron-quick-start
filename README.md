# electron-quick-start

This is a minimal Electron application based on the [Quick Start Guide](https://electronjs.org/docs/tutorial/quick-start) within the Electron documentation which demonstrates how to use Radiant Media Player with DASH and Widevine DRM.

A basic Electron application needs just these files:

- `package.json` - Points to the app's main file and lists its details and dependencies.
- `main.js` - Starts the app and creates a browser window to render HTML. This is the app's **main process**.
- `index.html` - A web page to render. This is the app's **renderer process**.

You can learn more about each of these components within the Electron [Quick Start Guide](https://electronjs.org/docs/tutorial/quick-start).

## To Use
From your command line:

```bash
# Clone this repository
git clone https://github.com/radiantmediaplayer/electron-quick-start.git
# Go into the repository
cd electron-quick-start
# Install dependencies
npm install
# Configure index.html with your Radiant Media Player license key
# Run the app
npm start
```

## Documentation for using Radiant Media Player with DASH and Widevine DRM in an Electron app

Our set up is based on [castLabs Electron for Content Security](https://github.com/castlabs/electron-releases). In `package.json` you can see that devDependencies for electron points to https://github.com/castlabs/electron-releases#v6.0.4-wvvmp. This set up has been tested with version 6.0.4 of castLabs Electron for Content Security and Radiant Media Player version 5.4.8.
In `index.html` we have our player configured to use DASH with Widevine DRM.
In `main.js` we have made changes in order to automatically prepare our application to support Widevine DRM. 
Please review the above changes before moving forward.

## Supported Widevine DRM feature

While this demo app just shows the core principle for using Radiant Media Player with DASH and Widevine DRM, the following features are supported:
- Playback of Widevine DRM encrypted content with DASH or HLS 
- Support for Widevine Verified Media Path
- Features generally available with Radiant Media Player when using [DASH and Widevine DRM](https://www.radiantmediaplayer.com/docs/latest/dash-drm-documentation.html)

To achieve this the necessary Widevine DRM components will be installed on first launch and enabled as an option for playback of DRM protected content using common EME APIs.
For more advanced use-cases see [castLabs Electron for Content Security documentation](https://github.com/castlabs/electron-releases).

Currently unsupported and untested feature:
- Protected storage of licenses for offline playback scenarios

## Supported environments
- Windows 7+
- macOS 10.10+
- Linux Ubuntu 12.04+, Fedora 21+ and Debian 8+ (lacking support for persistent licenses due to VMP limitations)

## License

[CC0 1.0 (Public Domain)](LICENSE.md) for this GitHub repository.
Radiant Media Player is a commercial HTML5 video player with [its own terms of use](https://www.radiantmediaplayer.com/terms-of-service.html).
