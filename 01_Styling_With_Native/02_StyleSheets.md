1. We can split our component into 2 sections, the component and the styles.
2. import `StyleSheet` from `react-native`.

```js
import { StyleSheet } from 'react-native';
```

3. At the bottom of the file, we will create a `styles` object.

```js
const styles = StyleSheet.create({});
```

4. Now we can move our styles into the `styles` object.

```js
const styles = StyleSheet.create({
  container: {
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
  },
});
```

5. Now we can use our styles in our component.

```js
const ListItem = () => {
  return (
    <View style={styles.container}>
      <Text>List Item</Text>
    </View>
  );
};
```

6. Let's continue with our card component.

```js
const ListItem = () => {
  return (
    <View style={styles.card}>
      <View style={styles.row}>
        <View style={styles.container}>
          <Image
            source={{ uri: 'https://picsum.photos/200/300' }}
            resizeMode="contain"
            style={styles.image}
          />
        </View>
        <View style={{ marginLeft: 12 }}>
          <Text style={styles.title}>Title</Text>
          <Text
            style={{
              marginTop: 4,
              color: 'gray',
              fontSize: 12,
            }}
          >
            Description
          </Text>
        </View>
      </View>
      <View style={styles.badge}>
        <Text style={{ color: '#fff' }}>0</Text>
      </View>
    </View>
  );
};
```

7. And our styles for our card component.

```js
const styles = StyleSheet.create({
  card: {
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
  },
  container: {
    height: 50,
    width: 50,
    borderRadius: 25,
    backgroundColor: '#fff',
    borderColor: '#eee',
    borderWidth: 1,
    borderStyle: 'solid',
    alignItems: 'center',
    justifyContent: 'center',
  },
  image: {
    borderRadius: 25,
    height: 50,
    width: 50,
  },
  row: { flexDirection: 'row', alignItems: 'center' },
  badge: {
    height: 25,
    backgroundColor: 'teal',
    borderWidth: 0,
    width: 25,
    marginLeft: -26,
    alignItems: 'center',
    justifyContent: 'center',
    borderRadius: 50,
  },
  title: {
    fontSize: 14,
    color: 'black',
    fontWeight: 'bold',
    textTransform: 'capitalize',
  },
});
```
