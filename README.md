# reactNativeONNX

<h2>
Prerequisites
</h2>

Before you get started with React Native and ONNX, make sure you have the following prerequisites in place:

1. Install Expo

Follow the official Expo installation guide to install Expo on your development machine: 

`https://docs.expo.dev/get-started/installation/`

<h2>Create a project</h2>

1. Initialize a new project
```
npx create-expo-app my-app 

cd my-app
```

2. Install `onnxruntime-react-native` package.

```
expo install onnxruntime-react-native@latest
```

3. Modify `metro.config.js` to

```
// Learn more https://docs.expo.io/guides/customizing-metro
const { getDefaultConfig } = require("expo/metro-config");

/** @type {import('expo/metro-config').MetroConfig} */
const config = getDefaultConfig(__dirname);
config.resolver.assetExts.push("onnx");
module.exports = config;
```

4. Update `"plugins": ["onnxruntime-react-native"]` to `app.json`

```
{
  "expo": {
    "name": "reactNativeONNX",
    "slug": "reactNativeONNX",
    "plugins": ["onnxruntime-react-native"],
    "version": "1.0.0",
    "assetBundlePatterns": ["**/*"]
  }
}
```

5. Build the Project
```
npx expo prebuild
```

6. Run the App

```
npx expo run:ios

npx expo run:android
```

This setup will allow you to start building React Native applications with ONNX for machine learning. Make sure to refer to the official documentation and resources for further development and customization.