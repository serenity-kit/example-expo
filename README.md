How to:

1. Setup an Expo project
2. Setup EAS:

```sh
eas build:configure
```

3. Add a simulator build to eas.json

```json
{
  "build": {
    "development-simulator": {
      "developmentClient": true,
      "distribution": "internal",
      "ios": {
        "simulator": true
      }
    }
  }
}
```

4. Add expo-dev-client to package.json

```sh
npx expo install expo-dev-client
```

Add this to the top of App.js

```js
import "expo-dev-client";
```

Replace in package.json:

```json
"start": "expo start",
"android": "expo start --android",
"ios": "expo start --ios",
"web": "expo start --web"
```

with:

```json
"start": "expo start --dev-client",
"android": "expo start --android --dev-client",
"ios": "expo start --ios --dev-client",
"web": "expo start --web --dev-client"
```

5. Commit your changes

6. Add react-native-opaque

```sh
npx expo install react-native-opaque
```

7. Run a build

```sh
eas build --profile development-simulator --platform ios
```
