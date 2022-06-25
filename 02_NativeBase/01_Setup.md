Another alternative to using css in react native, is a library called native base.

1. Install native base.

```js
$ npm install native-base styled-components styled-system
```

2. In `App.js` Import NativeBaseProvider from 'native-base':

```js
import { NativeBaseProvider } from 'native-base';
```

3. Wrap your main component in `app.js` with `NativeBaseProvider`

```js
<NativeBaseProvider>
  <View style={styles.container}>
    <ListItem />
  </View>
</NativeBaseProvider>
```
