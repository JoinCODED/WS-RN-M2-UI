In VSCode, open `App.js` which is the application's starting point. Note that we're not using JSX tags, we're importing and rendering pre-built components from `react-native`.

Take a look at the [documentation](https://reactnative.dev/docs/components-and-apis#basic-components) to learn more about the basic components.

We will use those components to create a simple card component.

Fork and clone [this](https://github.com/JoinCODED/Demo-RN-M2-UI) into your development folder.

1. Create a new folder called `components` and move into it.
2. Create a new file called `ListItem.js` and move into it.

```js
const ListItem = () => {};
export default ListItem;
```

3. Let's import the required components from `react-native`.

```js
import React from 'react';
import { Image, Text, View } from 'react-native';
```

4. To style in react native, every component have a `style` property.

5. We will start by adding a `View` component. This component is used to wrap other components. Just like a `div` in HTML.

```js
<View style={{}}></View>
```

6. We can't write pure CSS, we need to use javascript to style our components. Here's some examples:

```
css: background-color: #fff;
js: backgroundColor: '#fff'
```

7. You can use this website to convert CSS to JS: [css-to-js](https://css-to-js.converter.online/).

8. So to style our `View`:

```js
<View
  style={{
    height: 90,
    alignItems: 'center',
    justifyContent: 'center',
    backgroundColor: '#fff',
    borderRadius: 15,
    shadowColor: 'gray',
    shadowOffset: { width: 0, height: 0 },
    shadowOpacity: 1,
    shadowRadius: 8,
    elevation: 8,
    flexDirection: 'row',
    justifyContent: 'space-between',
    paddingLeft: 16,
    paddingRight: 14,
    marginTop: 6,
    marginBottom: 6,
    marginLeft: 16,
    marginRight: 16,
  }}
></View>
```

9. Ew, that's a lot of styling code nested into the view, there should be another way.
