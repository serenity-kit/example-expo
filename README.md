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
