# React Native Camera

# 🚧 🚧 🚧

## React Native Camera is deprecated!

This project aims to fix React Native Camera deprecations with new versions of React Native.

If you are using `react-native-camera` with new versions of `react-native` you are probably seeing the following message:

```txt
ViewPropTypes will be removed from React Native. Migrate to ViewPropTypes exported from 'deprecated-react-native-prop-types'.
```

See this [issue](https://github.com/facebook/react-native/issues/33557)

## For Your Information

I fixed the `ViewPropTypes` import and now it is not necessary to implement a workaround with Babel.

You can continue to use `react-native-camera` in your project without any code changes, but consider upgrading to [react-native-vision-camera](https://github.com/mrousavy/react-native-vision-camera) in the future.

VisionCamera offers new APIs, better performance, improved stability and more features.
It is actively maintained by [**@mrousavy**](https://github.com/mrousavy) and used in many production apps.

You can support the development of VisionCamera by [sponsoring **@mrousavy** on GitHub](https://github.com/sponsors/mrousavy).

## Docs
Follow the `react-native-camera` docs here [https://react-native-camera.github.io/react-native-camera/](https://react-native-camera.github.io/react-native-camera/)

Supports:

- photographs.
- videos
- face detection (Android & iOS only)
- barcode scanning
- text recognition (optional installation for iOS using CocoaPods)

### Example import

```jsx
import { RNCamera, FaceDetector } from 'react-native-camera';
```

#### How to use master branch?

We recommend using the releases from npm, however if you need some features that are not published on npm yet you can install react-native-camera from git.

**yarn**: `yarn add react-native-camera@git+https://git@github.com/caiosdias/react-native-camera.git`

**npm**: `npm install --save react-native-camera@git+https://git@github.com/caiosdias/react-native-camera.git`

##### Permissions

To use the camera,

1) On Android you must ask for camera permission:

```java
  <uses-permission android:name="android.permission.CAMERA" />
```

To enable `video recording` feature you have to add the following code to the `AndroidManifest.xml`:

```java
  <uses-permission android:name="android.permission.RECORD_AUDIO"/>
  <uses-permission android:name="android.permission.READ_EXTERNAL_STORAGE" />
  <uses-permission android:name="android.permission.WRITE_EXTERNAL_STORAGE" />
```

![5j2jduk](https://cloud.githubusercontent.com/assets/2302315/22190752/6bc6ccd0-e0da-11e6-8e2f-6f22a3567a57.gif)

2) On iOS, you must update Info.plist with a usage description for camera

```xml
...
<key>NSCameraUsageDescription</key>
<string>Your own description of the purpose</string>
...
	
```
For more information on installation, please refer to [installation requirements](./docs/installation.md#requirements).

For general introduction, please take a look into this [RNCamera](./docs/RNCamera.md).
