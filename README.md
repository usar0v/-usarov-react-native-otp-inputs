### Expo is currently not supported as `Clipboard` is not included in Expo SDK

```bash
$ yarn add @usarov/react-native-otp-inputs @react-native-clipboard/clipboard
```

### After installation run:

```bash
$ npx pod-install
```

Clipboard module has been extracted from react-native core, so it needs to be installed separately.
Package uses it for autofill feature

<details>
  <summary>For React Native version 0.59</summary>

### React Native <= 0.59

run the following command to link the package:

```
$ react-native link @react-native-clipboard/clipboard
```

For iOS, make sure you install the pod file.

```
cd ios && pod install && cd ..
```

</details>


## Basic usage

```js
import React, { useState } from 'react';
import { View } from 'react-native';
import OtpInputs from '@usarov/react-native-otp-inputs';

export const App = () => {
const [code, setCode] = useState('');

    return (
      <View flex={1}>
        <OtpInputs
          defaultValue={code}
          autoFocus
          handleChange={setCode}
          inputStyles={{ textAlign: 'center' }}
          numberOfInputs={4}
        />
      </View>
    );
}
```

## [API](./docs/API.md)

### Contributors

Great thanks to :
[@usarov](https://github.com/usar0v).
