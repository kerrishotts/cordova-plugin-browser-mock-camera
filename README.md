# Camera Browser Mock Plugin

> **WARNING:** This plugin is **NOT** intended for production use. It is currently just a _proof of concept_.

This plugin mocks the Camera API in the browser platform. It requires that the `browser` platform has been added to your project, and that `cordova-plugin-browser-mock` has also been added.

## Installation

```
$ cordova platform add browser
$ cordova plugin add --save cordova-plugin-browser-mock
$ cordova plugin add --save cordova-plugin-browser-mock-camera
```

## Usage

Installing the plugin will automatically mock the API. When you call `navigator.camera.getPicture`, your success callback will be called with a base64 image.

If you wish your failure callback to be called, you can tell the mock to fail:

```
cordova.plugins.browser.mock.camera.mockOptions.fail = true;
```

After this calls to `navigator.camera.getPicture` will call your failure callback with an error.

## License

MIT
