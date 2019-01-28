# react-native-fast-storage

react-native-fast-storage is a drop in replacement for `AsyncStorage`.

This library is the React Native implementation of https://github.com/Tencent/MMKV.

It provides very fast read and write access.

## Getting started

`$ yarn add  'https://github.com/nkabir1986/react-native-fast-storage.git#v1.0.17'`

`$ react-native link react-native-fast-storage`

**Additional IOS step**

in pod file add below line:

`$ pod 'MMKV'`

and after that run pod install

## Usage

```javascript
import FastStorage from "react-native-fast-storage";

await FastStorage.setItem("key", "Coucou toi");

const item = await FastStorage.getItem("key");
```

## Methods

All methods are asynchronous, just like AsyncStorage.

| Prop       |     Params      | Returns  | Description                    |
| :--------- | :-------------: | :------: | :----------------------------- |
| setItem    |  `key`, `value` |  `value` |  Allows to set an item         |
| getItem    |      `key`      |  `value` |  Retrieve the item             |
| removeItem |      `key`      |   null   |  Remove an item from the store |
| clearStore |       none      |   null   |  Clear the entire store        |
