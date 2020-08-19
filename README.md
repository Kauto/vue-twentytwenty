# Vue-TwentyTwenty-One

[![npm](https://img.shields.io/npm/v/vue-twentytwenty-one.svg)
![npm](https://img.shields.io/npm/dm/vue-twentytwenty-one.svg)](https://www.npmjs.com/package/vue-twentytwenty-one)
[![vue2](https://img.shields.io/badge/vue-2.x-brightgreen.svg)](https://vuejs.org/)

A small component to quickly let users see the differences between 2 images. This is a fork of [vue-twentytwenty](https://www.npmjs.com/package/vue-twentytwenty).

## Installation

```
$ npm install vue-twentytwenty-one
```

##git  Usage

```js
import 'vue-twentytwenty-one/dist/vue-twentytwenty-one.css';
import TwentyTwenty from 'vue-twentytwenty-one';

export default {
  // ...
  components: {
    TwentyTwenty
  },
  data() {
    return {
      offset: 0.5
    }
  }
  // ...
};
```

It can then be used like so:

```html
<TwentyTwenty
  v-model="offset"
  before="//placehold.it/600x200/E8117F/FFFFFF"
  after="//placehold.it/600x200/CCCCCC/FFFFFF" />
```

## Props
|Props|Description|Required|Type|Default|
|-----|-----------|--------|----|-------|
|before|URL of before image|true|String|-|
|beforeLabel|When hovering over image what label should show up over before image|false|String|-|
|after|URL of after image|true|String|-|
|afterLabel|When hovering over image what label should show up over after image|false|String|-|
|value|How far from the left the slider should be on load (between 0 and 1)|false|Number|0.5|
|keyboardStep|How far the slider should be moved on arrow key press (between 0 and 1)|false|Number|0.2|
|lock|Locks the 20-20, so the offset can't be changed|false|Boolean|false|

## Events
|Event|Description|
|-----|-----------|
|input|Triggered when the offset changes|
|click|Triggered if the Twentytwenty is clicked without moving the slider|
